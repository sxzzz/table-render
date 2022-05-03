<template>
  <div id="app">
    <staff-table :staff="staff"></staff-table>
  </div>
</template>

<script>
/* eslint-disable vue/no-unused-components */
import StaffTable from './components/StaffTableWithSearchBar.vue'

// Data source
function getStaff() {
  return [
	{
		"id" : 1,
		"department" : "Photography",
		"occupation" : "",
		"first_name" : "Michael",
		"last_name" : "Arber",
		"user_name" : "Mick"
	},
	{
		"id" : 2,
		"department" : "Pre-Press",
		"occupation" : "",
		"first_name" : "Claire",
		"last_name" : "Evans",
		"user_name" : "Claire"
	},
	{
		"id" : 3,
		"department" : "Pre-Press",
		"occupation" : "",
		"first_name" : "Chris",
		"last_name" : "Raggett",
		"user_name" : "Chris"
	},
	{
		"id" : 4,
		"department" : "Management",
		"occupation" : "",
		"first_name" : "Lynn",
		"last_name" : "Rennie",
		"user_name" : "LynnR"
	},
	{
		"id" : 5,
		"department" : "Photography",
		"occupation" : "MD",
		"first_name" : "Tony",
		"last_name" : "Wouters",
		"user_name" : "Tony"
	},
	{
		"id" : 6,
		"department" : "Management",
		"occupation" : "",
		"first_name" : "Jarrod",
		"last_name" : "Wouters",
		"user_name" : "Jarrod"
	},
	{
		"id" : 7,
		"department" : "Photography",
		"occupation" : "",
		"first_name" : "Teagan",
		"last_name" : "Wouters",
		"user_name" : "Teagan"
	},
	{
		"id" : 8,
		"department" : "AM",
		"occupation" : "",
		"first_name" : "Natalie",
		"last_name" : "Sargeant",
		"user_name" : "Nat"
	},
	{
		"id" : 9,
		"department" : "Photography",
		"occupation" : "",
		"first_name" : "Mandy",
		"last_name" : "Wouters",
		"user_name" : "Mandy"
	},
	{
		"id" : 10,
		"department" : "Finance",
		"occupation" : "Accountant",
		"first_name" : "Deb",
		"last_name" : "Washington",
		"user_name" : "DWashington"
	},
	{
		"id" : 11,
		"department" : "Sales & Marketing",
		"occupation" : "Sales & Marketing Manager",
		"first_name" : "Suzanne",
		"last_name" : "Phillips",
		"user_name" : "suep"
	},
	{
		"id" : 12,
		"department" : "School Care",
		"occupation" : "",
		"first_name" : "Susan",
		"last_name" : "Rawlins",
		"user_name" : "SusanR"
	},
	{
		"id" : 13,
		"department" : "Photography",
		"occupation" : "Photographer",
		"first_name" : "Kylie",
		"last_name" : "Haley",
		"user_name" : "KylieH"
	},
	{
		"id" : 14,
		"department" : "Photography",
		"occupation" : "Fam. Port Sales / Photographer",
		"first_name" : "Deanne",
		"last_name" : "Kampe",
		"user_name" : "DeanneK"
	},
	{
		"id" : 15,
		"department" : "Pre-Press",
		"occupation" : "HR Consultant",
		"first_name" : "Deborah",
		"last_name" : "Peppard",
		"user_name" : "DeborahP"
	},
	{
		"id" : 16,
		"department" : "Pre-Press",
		"occupation" : "Lab",
		"first_name" : "Juliana",
		"last_name" : "Petrusic",
		"user_name" : "julianap"
	},
	{
		"id" : 17,
		"department" : "Photography",
		"occupation" : "Photographer",
		"first_name" : "Heath",
		"last_name" : "Wouters",
		"user_name" : "HeathW"
	},
	{
		"id" : 18,
		"department" : "IT",
		"occupation" : "IT and Database Programmer",
		"first_name" : "Joseph",
		"last_name" : "Hilltop",
		"user_name" : "JHilltop"
	},
	{
		"id" : 19,
		"department" : "Photography",
		"occupation" : "Photographer",
		"first_name" : "Olav",
		"last_name" : "Dias",
		"user_name" : "OlavD"
	},
	{
		"id" : 20,
		"department" : "Customer Service",
		"occupation" : "Packing Team Leader",
		"first_name" : "Carly",
		"last_name" : "West",
		"user_name" : "CarlyW"
	},
	{
		"id" : 21,
		"department" : "Pre-Press",
		"occupation" : "Lab Team Member",
		"first_name" : "Shannon",
		"last_name" : "Nutt",
		"user_name" : "SNutt"
	},
	{
		"id" : 22,
		"department" : "IT",
		"occupation" : "Database Administrator",
		"first_name" : "David",
		"last_name" : "Muir",
		"user_name" : "DMuir"
	},
	{
		"id" : 23,
		"department" : "School Care",
		"occupation" : "Data Management Team Leader",
		"first_name" : "Jocelyn",
		"last_name" : "Edwards",
		"user_name" : "Jocelyn"
	},
	{
		"id" : 24,
		"department" : "Customer Service",
		"occupation" : "Receptionist/Administrative Assistant",
		"first_name" : "Pamela",
		"last_name" : "Aitken",
		"user_name" : "PamelaA"
	},
	{
		"id" : 25,
		"department" : "School Care",
		"occupation" : "Data Team Member",
		"first_name" : "Amanda",
		"last_name" : "Gibson",
		"user_name" : "AmandaG"
	},
	{
		"id" : 26,
		"department" : "Packing",
		"occupation" : "Packer",
		"first_name" : "Jayde",
		"last_name" : "Keith",
		"user_name" : "JaydeK"
	},
	{
		"id" : 27,
		"department" : "Photography",
		"occupation" : "Money Counter",
		"first_name" : "Cheryl",
		"last_name" : "Lind",
		"user_name" : "CherylL"
	},
	{
		"id" : 28,
		"department" : "Packing",
		"occupation" : "Packer",
		"first_name" : "Fiona",
		"last_name" : "McDonald",
		"user_name" : "FionaM"
	},
	{
		"id" : 29,
		"department" : "IT",
		"occupation" : "Web Developer",
		"first_name" : "Andrew",
		"last_name" : "Burch",
		"user_name" : "AndrewB"
	},
	{
		"id" : 30,
		"department" : "Pre-Press",
		"occupation" : "Lab Team Member",
		"first_name" : "Jacqueline",
		"last_name" : "Grunberg",
		"user_name" : "JacquelineG"
	},
	{
		"id" : 31,
		"department" : "Packing",
		"occupation" : "Packing Team Member",
		"first_name" : "Aimie",
		"last_name" : "Clydesdale",
		"user_name" : "AimieC"
	},
	{
		"id" : 32,
		"department" : "Photography",
		"occupation" : "Photographer",
		"first_name" : "Ruth",
		"last_name" : "Yates",
		"user_name" : "RuthY"
	},
	{
		"id" : 33,
		"department" : "Photography",
		"occupation" : "Money",
		"first_name" : "Leonie",
		"last_name" : "Wainwright",
		"user_name" : "LeonieW"
	},
	{
		"id" : 34,
		"department" : "Pre-Press",
		"occupation" : "Lab Team Leader",
		"first_name" : "Scott",
		"last_name" : "Taylor",
		"user_name" : "Scott"
	},
	{
		"id" : 35,
		"department" : "IT",
		"occupation" : "",
		"first_name" : "Mark",
		"last_name" : "Ricketts",
		"user_name" : "MarkR"
	},
	{
		"id" : 36,
		"department" : "Photography",
		"occupation" : "Photography Assistant",
		"first_name" : "Vicki",
		"last_name" : "Pincombe",
		"user_name" : "VickiP"
	},
	{
		"id" : 37,
		"department" : "Customer Service",
		"occupation" : "Customer Service Team Member",
		"first_name" : "Angela",
		"last_name" : "Nel",
		"user_name" : "AngelaN"
	},
	{
		"id" : 38,
		"department" : "Packing",
		"occupation" : "Packing Team Member",
		"first_name" : "Antonia",
		"last_name" : "Hird",
		"user_name" : "AntoniaH"
	},
	{
		"id" : 39,
		"department" : "Packing",
		"occupation" : "Packing Team Member",
		"first_name" : "Caitlin",
		"last_name" : "Welsford",
		"user_name" : "CaitlinW"
	},
	{
		"id" : 40,
		"department" : "Photography",
		"occupation" : "Photographer",
		"first_name" : "Naomi",
		"last_name" : "Pommerel",
		"user_name" : "NaomiP"
	},
	{
		"id" : 41,
		"department" : "IT",
		"occupation" : "",
		"first_name" : "NothingButWeb",
		"last_name" : "API Access",
		"user_name" : "nothingbutweb"
	},
	{
		"id" : 42,
		"department" : "IT",
		"occupation" : "",
		"first_name" : "OnlineOrdering",
		"last_name" : "API Access",
		"user_name" : "onlineordering"
	},
	{
		"id" : 43,
		"department" : "IT",
		"occupation" : null,
		"first_name" : "PrintManager",
		"last_name" : "API Access",
		"user_name" : "printmanager"
	},
	{
		"id" : 44,
		"department" : "Photography",
		"occupation" : "Photography Team Manager",
		"first_name" : "Christine",
		"last_name" : "Madden",
		"user_name" : "ChristineM"
	},
	{
		"id" : 45,
		"department" : "IT",
		"occupation" : "",
		"first_name" : "Staff Website",
		"last_name" : "API Access",
		"user_name" : "staffwebsite"
	},
	{
		"id" : 46,
		"department" : "Pre-Press",
		"occupation" : "",
		"first_name" : "PDFAssembler",
		"last_name" : "API Access",
		"user_name" : "pdfassembler"
	},
	{
		"id" : 47,
		"department" : "Photography",
		"occupation" : "Photographer",
		"first_name" : "Claire",
		"last_name" : "Roberts",
		"user_name" : "ClaireR"
	},
	{
		"id" : 48,
		"department" : "Photography",
		"occupation" : "Photographer",
		"first_name" : "Barbara",
		"last_name" : "Bradlington",
		"user_name" : "BarbaraB"
	},
	{
		"id" : 49,
		"department" : "Photography",
		"occupation" : "Photographer",
		"first_name" : "Rob",
		"last_name" : "Moore",
		"user_name" : "RobM"
	},
	{
		"id" : 50,
		"department" : "Pre-Press",
		"occupation" : "Lab Team Member",
		"first_name" : "Meredith",
		"last_name" : "French",
		"user_name" : "MeredithF"
	},
	{
		"id" : 51,
		"department" : "Smart Practice",
		"occupation" : "Smart Practice",
		"first_name" : "Sarah",
		"last_name" : "Matthews",
		"user_name" : "SarahM"
	},
	{
		"id" : 52,
		"department" : "Pre-Press",
		"occupation" : "Smart Practice",
		"first_name" : "Christine",
		"last_name" : "Wouters",
		"user_name" : "ChristineW"
	},
	{
		"id" : 53,
		"department" : "Photography",
		"occupation" : "JosephD",
		"first_name" : "Joseph",
		"last_name" : "DeRose",
		"user_name" : "JosephD"
	},
	{
		"id" : 54,
		"department" : "Photography",
		"occupation" : "Photographer",
		"first_name" : "Crystalyn",
		"last_name" : "Cordwell",
		"user_name" : "CrystalynC"
	},
	{
		"id" : 55,
		"department" : "Photography",
		"occupation" : "Photograher",
		"first_name" : "Gaynor",
		"last_name" : "Muller",
		"user_name" : "GaynorM"
	},
	{
		"id" : 56,
		"department" : "Photography",
		"occupation" : "Photographer",
		"first_name" : "Mads",
		"last_name" : "Park",
		"user_name" : "MadelineP"
	},
	{
		"id" : 57,
		"department" : "Photography",
		"occupation" : "Photographer",
		"first_name" : "Chloe",
		"last_name" : "Jones",
		"user_name" : "ChloeJ"
	},
	{
		"id" : 58,
		"department" : "Photography",
		"occupation" : "Photographer",
		"first_name" : "Stan",
		"last_name" : "Samantzis",
		"user_name" : "StanS"
	},
	{
		"id" : 59,
		"department" : "Photography",
		"occupation" : "Photographer",
		"first_name" : "Shell",
		"last_name" : "Roberts",
		"user_name" : "MichelleR"
	},
	{
		"id" : 60,
		"department" : "Pre-Press",
		"occupation" : "Pre Press",
		"first_name" : "Lucy",
		"last_name" : "Woolmore",
		"user_name" : "LucyW"
	},
	{
		"id" : 61,
		"department" : "Pre-Press",
		"occupation" : "Pre Press",
		"first_name" : "Sandra",
		"last_name" : "Baquero",
		"user_name" : "SandraB"
	},
	{
		"id" : 62,
		"department" : "Packing",
		"occupation" : "Packing",
		"first_name" : "Annette",
		"last_name" : "Prinzi",
		"user_name" : "AnnetteP"
	},
	{
		"id" : 63,
		"department" : "Packing",
		"occupation" : "Packing",
		"first_name" : "Julie",
		"last_name" : "Renton",
		"user_name" : "JulieR"
	},
	{
		"id" : 64,
		"department" : "Packing",
		"occupation" : "Packing",
		"first_name" : "Amanda",
		"last_name" : "Fitzpatrick",
		"user_name" : "AmandaF"
	},
	{
		"id" : 65,
		"department" : "Packing",
		"occupation" : "School Care Team Member",
		"first_name" : "Tyler",
		"last_name" : "Smith",
		"user_name" : "TylerS"
	},
	{
		"id" : 66,
		"department" : "Photography",
		"occupation" : "Photographer",
		"first_name" : "Ken",
		"last_name" : "Nakanishi",
		"user_name" : "KenN"
	},
	{
		"id" : 67,
		"department" : "Photography",
		"occupation" : "Photographer",
		"first_name" : "Kira",
		"last_name" : "Sharkie",
		"user_name" : "kiras"
	},
	{
		"id" : 68,
		"department" : "Photography",
		"occupation" : "Photographer",
		"first_name" : "Daniel",
		"last_name" : "Auricchio",
		"user_name" : "Daniel"
	},
	{
		"id" : 69,
		"department" : "Photography",
		"occupation" : "Photographer",
		"first_name" : "Sam",
		"last_name" : "Dunn",
		"user_name" : "SamD"
	},
	{
		"id" : 70,
		"department" : "Photography",
		"occupation" : "Photographer",
		"first_name" : "Luca",
		"last_name" : "Pisci",
		"user_name" : "LucaP"
	},
	{
		"id" : 71,
		"department" : "Photography",
		"occupation" : "Photographer",
		"first_name" : "Tina",
		"last_name" : "Accardo",
		"user_name" : "TinaA"
	},
	{
		"id" : 72,
		"department" : "Finance",
		"occupation" : "Finance Assistant",
		"first_name" : "Rachel",
		"last_name" : "MacDonald",
		"user_name" : "RachelM"
	},
	{
		"id" : 73,
		"department" : "School Care",
		"occupation" : "School Care Team Member",
		"first_name" : "Crystal",
		"last_name" : "Stevens",
		"user_name" : "CrystalS"
	},
	{
		"id" : 74,
		"department" : "Photography",
		"occupation" : "Photographer",
		"first_name" : "Nadja",
		"last_name" : "Herrmann",
		"user_name" : "NadjaH"
	},
	{
		"id" : 75,
		"department" : "Pre-Press",
		"occupation" : "",
		"first_name" : "Nathan",
		"last_name" : "Todd",
		"user_name" : "NathanT"
	},
	{
		"id" : 76,
		"department" : "Packing",
		"occupation" : "Packer",
		"first_name" : "Samantha",
		"last_name" : "Edwards",
		"user_name" : "SammyE"
	},
	{
		"id" : 77,
		"department" : "Packing",
		"occupation" : "Packer",
		"first_name" : "Amee",
		"last_name" : "Blake",
		"user_name" : "AmeeB"
	},
	{
		"id" : 78,
		"department" : "Packing",
		"occupation" : "Packer",
		"first_name" : "Samantha",
		"last_name" : "Sawyer",
		"user_name" : "SamanthaS"
	},
	{
		"id" : 79,
		"department" : "Pre-Press",
		"occupation" : "Pre Press Team Member",
		"first_name" : "Emily",
		"last_name" : "Horne",
		"user_name" : "EHorne"
	},
	{
		"id" : 80,
		"department" : "Packing",
		"occupation" : "Packer",
		"first_name" : "Krystal",
		"last_name" : "Sewell",
		"user_name" : "KrystalS"
	},
	{
		"id" : 81,
		"department" : "School Care",
		"occupation" : "Quality Control / Admin",
		"first_name" : "Christy",
		"last_name" : "Tobeck",
		"user_name" : "ChristyT"
	},
	{
		"id" : 82,
		"department" : "Photography",
		"occupation" : "Photographer",
		"first_name" : "Renee",
		"last_name" : "Brooker",
		"user_name" : "ReneeB"
	},
	{
		"id" : 83,
		"department" : "Photography",
		"occupation" : "Photographer",
		"first_name" : "Tasha",
		"last_name" : "Friede",
		"user_name" : "TashF"
	},
	{
		"id" : 84,
		"department" : "Photography",
		"occupation" : "Photographer",
		"first_name" : "Jacinta",
		"last_name" : "Theobold",
		"user_name" : "JacintaT"
	},
	{
		"id" : 85,
		"department" : "Photography",
		"occupation" : "Photographer",
		"first_name" : "Belinda",
		"last_name" : "Furletti",
		"user_name" : "BelindaF"
	},
	{
		"id" : 86,
		"department" : "Photography",
		"occupation" : "Photographer",
		"first_name" : "Mark",
		"last_name" : "Monro",
		"user_name" : "MarkM"
	},
	{
		"id" : 87,
		"department" : "AM",
		"occupation" : "Quality Control / Admin",
		"first_name" : "Alison",
		"last_name" : "West",
		"user_name" : "AlisonW"
	},
	{
		"id" : 88,
		"department" : "Photography",
		"occupation" : "Photographer",
		"first_name" : "Madeline",
		"last_name" : "Ward",
		"user_name" : "MadelineW"
	},
	{
		"id" : 89,
		"department" : "School Care",
		"occupation" : "School Care Team Member",
		"first_name" : "Jenny",
		"last_name" : "Vlug",
		"user_name" : "JennyV"
	},
	{
		"id" : 90,
		"department" : "School Care",
		"occupation" : "School Care Team Member",
		"first_name" : "Jemma",
		"last_name" : "Pawley",
		"user_name" : "JemmaP"
	},
	{
		"id" : 91,
		"department" : "Packing",
		"occupation" : "Packer",
		"first_name" : "Chantelle",
		"last_name" : "Cousens",
		"user_name" : "ChantelleC"
	},
	{
		"id" : 92,
		"department" : "Packing",
		"occupation" : "Packer",
		"first_name" : "Jeremy",
		"last_name" : "Cowell",
		"user_name" : "JeremyC"
	},
	{
		"id" : 93,
		"department" : "Packing",
		"occupation" : "Packer",
		"first_name" : "Felicity",
		"last_name" : "Jagusch",
		"user_name" : "FelicityJ"
	},
	{
		"id" : 94,
		"department" : "Photography",
		"occupation" : "Photographer",
		"first_name" : "James",
		"last_name" : "Older",
		"user_name" : "JamesO"
	},
	{
		"id" : 95,
		"department" : "School Care",
		"occupation" : "School Care Team Member",
		"first_name" : "Kristy",
		"last_name" : "Older",
		"user_name" : "KristyO"
	},
	{
		"id" : 96,
		"department" : "Sales & Marketing",
		"occupation" : "Graphic Designer",
		"first_name" : "Emma",
		"last_name" : "Pike",
		"user_name" : "emmap"
	},
	{
		"id" : 97,
		"department" : "School Care",
		"occupation" : "School Care Team Member",
		"first_name" : "Jeanne",
		"last_name" : "Carlos",
		"user_name" : "JeanneC"
	},
	{
		"id" : 98,
		"department" : "AM",
		"occupation" : "Account Manager",
		"first_name" : "Hayley",
		"last_name" : "Gleeson",
		"user_name" : "hayleyg"
	},
	{
		"id" : 99,
		"department" : "Photography",
		"occupation" : "Photographer",
		"first_name" : "Dave",
		"last_name" : "Khan",
		"user_name" : "DavidK"
	},
	{
		"id" : 100,
		"department" : "Photography",
		"occupation" : "Photographer",
		"first_name" : "Robert",
		"last_name" : "Chrisfield",
		"user_name" : "RobertC"
	}
];
}

export default {
  name: 'App',
  components: {StaffTable},
  data(){
    return {
      staff: []
    }
  },
  created: function(){
    // Get table data from remote data source.
    this.staff = getStaff();
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin:10px;
}
</style>
