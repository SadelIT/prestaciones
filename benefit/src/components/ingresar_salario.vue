<template>
  
 <div class="card" style="width: 18rem;">

  <div class="container">
<table class="table">
  <thead>
    <tr>
      <th scope="col">#</th>
      <th scope="col">Salary</th>
      <th scope="col">Comissions</th>
      <th scope="col">Total</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th scope="row">1</th>
      <td> <input type="text" placeholder="0.00"  @input="salary01 = $event.target.value" /></td>
      <td><input type="text" placeholder="0.00"  @input="comission01 = $event.target.value" /></td>
      <td>{{Total1}}</td>
      
      

      
    </tr>
    <tr>
      <th scope="row">2</th>
      <td><input type="text" placeholder="0.00" /></td>
      <td><input type="text" placeholder="0.00" /></td>
      <td>{{Total}}</td>
    </tr>
    <tr>
      <th scope="row">3</th>
        <td><input type="text" placeholder="0.00" /></td>
        <td><input type="text" placeholder="0.00" /></td>
      <td>{{Total}}</td>
    </tr>
    <tr>
      <th scope="row">4</th>
        <td><input type="text" placeholder="0.00" /></td>
        <td><input type="text" placeholder="0.00" /></td>
      <td>{{Total}}</td>
    </tr>
    <tr>
      <th scope="row">5</th>
        <td><input type="text" placeholder="0.00" /></td>
        <td><input type="text" placeholder="0.00" /></td>
      <td>{{Total}}</td>
    </tr>
    <tr>
      <th scope="row">6</th>
        <td><input type="text" placeholder="0.00" /></td>
        <td><input type="text" placeholder="0.00" /></td>
      <td>{{Total}}</td>
    </tr>
    <tr>
      <th scope="row">7</th>
        <td><input type="text" placeholder="0.00" /></td>
        <td><input type="text" placeholder="0.00" /></td>
      <td>{{Total}}</td>
    </tr>
        <tr>
      <th scope="row">8</th>
        <td><input type="text" placeholder="0.00" /></td>
        <td><input type="text" placeholder="0.00" /></td>
      <td>{{Total}}</td>
    </tr>
        <tr>
      <th scope="row">9</th>
        <td><input type="text" placeholder="0.00" /></td>
        <td><input type="text" placeholder="0.00" /></td>
      <td>{{Total}}</td>
    </tr>
        <tr>
      <th scope="row">10</th>
        <td><input type="text" placeholder="0.00" /></td>
        <td><input type="text" placeholder="0.00" /></td>
      <td>{{Total}}</td>
    </tr>
        <tr>
      <th scope="row">11</th>
        <td><input type="text" placeholder="0.00" /></td>
        <td><input type="text" placeholder="0.00" /></td>
      <td>{{Total}}</td>
    </tr>
        <tr>
      <th scope="row">12</th>
        <td><input type="text" placeholder="0.00" /></td>
        <td><input type="text" placeholder="0.00" /></td>
      <td>{{Total}}</td>
    </tr>
  </tbody>  
  </table>
 </div>

  
</div> 

       <button v-on:click="operacion()" class="btn btn-primary">Calculate</button>


</template>

<script>
export default {
  name: 'IngresarSalario',
  data() {
      return{
         Total1: null,
        Total: null,
        salary01: '',
        comission01: '',
         
      }

  },
 methods: {

   operacion: function(){

     this.Total1 = (this.salary01) + (this.comission01)

        

        
      


        


  





      }
   
 }




}
</script>