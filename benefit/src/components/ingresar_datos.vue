<template>
  <p>Salary: {{Salary1}}</p>

  <p> 
    <input class="inpu" type="number"   @input="salary = $event.target.value" >
    </p>

<div class="info">

  <p> soy result: {{result}}</p>

<p>ID: {{ id }}</p>
<input type="number" v-model="id" placeholder="ID" />  

<p>Name: {{ name }}</p>
<input v-model="name" placeholder="Name" />  

<p>Company: {{ company }}</p>
<input v-model="company" placeholder="Company" />  


</div>
<br>


<div class="datelaboral">





  <div class="calculate info">

 <!-- <input type="checkbox"  v-model="Ordinary" /> Ordinary
	<label for="checkbox">{{  }}</label>

  <input type="checkbox"  v-model="intermittent" />Intermittent
	<label for="checkbox">{{  }}</label> -->

  <input type="checkbox"  v-model="monthly" /> Monthly
	<label for="checkbox">{{  }}</label>

  <input type="checkbox"  v-model="fortnightly" /> Fortnightly
	<label for="checkbox">{{  }}</label>

  <input type="checkbox"  v-model="weekly" /> Weekly
	<label for="checkbox">{{  }}</label>

  <input type="checkbox"  v-model="diary" /> Diary
	<label for="checkbox">{{  }}</label>

  </div>

 <button v-on:click="operacion()" class="btn btn-primary">Calculate</button>


 </div>






  

 


  
</template>

<script>  

  //START JAVASCRIPT
  export default {
  name: 'IngresarDatos',
  data: function () {
        return {

          //START VAR OF CALCULATE
            weekly: null,
            fortnightly: null,
            diary: null,
            monthly: null,
          //END VAR CALCULATE
            Total: "",  
            salary: null,
            Salary1: null,
            salary01: null,
            comission01: null,

          //START VAR INFO
            id: "",
            name: "",
            company: "",
          //END VAR CALCULATE


          //START VAR DATE  
            date: '',
            startdate: null,
            enddate: null,
            mydate: '',
          //END VAR DATE

         
            starts: '',
            moment: '',


            picked: '',
            result: null


        }
    },
    methods:  {


    

      operacion: function(){

        

        
      


        if(this.monthly == true){
          this.result = parseInt(this.salary) + (10)
        }
        else{
           this.result = 0
        }


        


  





      }

     




      
    }

    
    
  }

  //END JAVASCRIPT

</script>



<style scoped>



.container{
  background-color: transparent;
    border: none;
    border-bottom: 1px solid #9e9e9e;
    border-radius: 0;
    outline: none;
    height: 3rem;
    width: 100%;
    font-size: 1rem;
    margin: 0 0 20px 0;
    padding: 0;
    box-shadow: none;
    box-sizing: content-box;
    transition: all .3s;



}




p {
  font-weight: bold;

}



</style>
