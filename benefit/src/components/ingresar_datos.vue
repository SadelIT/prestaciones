<template>





<div class="info">

<p>ID: {{ id }}</p>
<input type="number" v-model="id" placeholder="ID" />  

<p>Name: {{ name }}</p>
<input v-model="name" placeholder="Name" />  

<p>Company: {{ company }}</p>
<input v-model="company" placeholder="Company" />  


</div>
<br>


<div class="datelaboral">
  <p> Start Date:</p>
 <input class="startdate" type="date" v-model="startdate">
 <p> {{startdate}} </p>

  <p> End Date:</p>
  <input class="enddate" type="date" v-model="enddate">
 <p> {{enddate}} </p>

  
 </div>


  
</template>

<script>  

  //START JAVASCRIPT
  export default {
  name: 'IngresarDatos',
  data: function () {
        return {
            id: "",
            name: "",
            company: "",
            date: '',
            startdate: null,
            enddate: null,
            mydate: '',
  
            starts: '',
            moment: '',


        }
    },
    methods: function() {


      
    }
    
    
  }

  //END JAVASCRIPT

</script>



<style scoped>








p {
  font-weight: bold;

}

.date{
  
}



</style>