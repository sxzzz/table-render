<template>
  <div class="hello">
    <div class="row g-3 align-items-center">
        <div class="col-auto">
            <label for="inputDept" class="col-form-label">Department</label>
        </div>
        <div class="col-auto">
            <input type="text" id="inputDept" class="form-control" v-model="keyword">
        </div>
        <div class="col-auto">
            <button type="submit" class="btn btn-primary" @click="doSearch">Search</button>
            <button class="btn btn-secondary ml-2" @click="doClear">Clear</button>
        </div>
    </div>

    <hr>

    <table class="table">
        <thead>
            <tr>
                <th>ID</th>
                <th>Department</th>
                <th>Name</th>
                <th>Occupation</th>
                <th>Username</th>
            </tr>
        </thead>
        <tbody>
            <tr v-for="(item, index) in staffList" :key="item.id" :class="rowClassGenerator(index+1)">
                <td>
                    {{ item.id }}
                </td>
                <td @click="doSearch2(item.department)">
                    {{ item.department }}
                </td>
                <td>
                    {{ item.first_name }} {{ item.last_name}}
                </td>
                <td>
                    {{ item.occupation }}
                </td>
                <td>
                    {{ item.user_name }}
                </td>
            </tr>
        </tbody>
    </table>
  </div>
</template>

<script>
export default {
  name: 'StaffTable',
  props: {
    staff: {
        type: Array
    }
  },
  data(){
     return {
         keyword: '',
         staffList:[],
     } 
  },
  created:function(){
      this.staffList = this.staff;
  },
  methods:{
      rowClassGenerator: function(index){
          let cls = '';
          if(index % 3 === 0){
              cls = 'row-bold';
          }
          
          if(index % 5 ===0){
              cls += ' row-italic';
          }
          return cls;
      },
      doSearch: function(){
          const k = this.keyword.trim();

          if(k.length > 0){
              // keywork can not be empty string 
              // Clear current staff list
              this.staffList = [];
              // Check each row in staff, if match keywork, then appended into staff list
              this.staff.forEach(element => {
                  if(element.department.toUpperCase().indexOf(k.toUpperCase()) > -1){
                      this.staffList.push(element)
                  }
              });
          }else{
              // Show all staff
              this.staffList = this.staff;
          } 
      },
      doClear: function(){
          this.keyword = '';
          this.staffList = this.staff;
      },
      doSearch2: function(txt){
          this.keyword = txt;
          this.doSearch();
      }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.row-bold{
    font-weight: bold;
}
.row-italic{
    font-style: italic;
}
.ml-2{
    margin-left: 10px;
}
</style>
