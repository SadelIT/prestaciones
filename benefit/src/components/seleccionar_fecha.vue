<template>
   
  <div class="datelaboral">
<p> Start Date:{{d1}}</p>
 <input type="date" v-model="mydate" />

  <p> End Date:{{d2}}</p>
 <input type="date" v-model="mydate2" />
   <br>
 <span>Year:{{Year}}</span> <span>Months: {{Months}}</span><span>Days:{{Days}}</span>

  
 </div>

 <br>


 <button v-on:click="difference()" class="btn btn-primary">difference</button>


  
</template>

<script>
export default {
  name: 'SeleccionarFecha',
  data() {
    return {
      mydate2: '',
      mydate: '',
      d1: '',
      d2: '',
      moment: '',
      days: '',
      months: '',
      years: '',
      Period: ''
        


    }
  },
  methods: {
     difference: function () {
       
       this.d1 = this.mydate
       this.d2 = this.mydate2
       

       const firts = new Date(this.mydate);
       const second = new Date(this.mydate2);
       const diff = second - firts;
       const years = Math.floor(diff / (1000 * 60 * 60 * 24 * 365));
       const months = Math.floor((diff % (1000 * 60 * 60 * 24 * 365)) / (1000 * 60 * 60 * 24 * 30));
       const days = Math.floor(((diff % (1000 * 60 * 60 * 24 * 365)) % (1000 * 60 * 60 * 24 * 30)) / (1000 * 60 * 60 * 24));
       
    
        this.Year = (years)
        this.Months = (months)
        this.Days = (days)
        console.log(firts,second,diff,months,days,years)

  
  }
  }
  

}
</script>