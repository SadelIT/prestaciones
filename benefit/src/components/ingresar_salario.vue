<template>


  <Ingresardatos></Ingresardatos>



  <br>
 <div class="card" style="width: 35rem;">

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
      <td> <input type="number" placeholder="0.00"  @input="salary01 = $event.target.value" /></td>
      <td><input type="number" placeholder="0.00"  @input="comission01 = $event.target.value" /></td>
      <td>{{Total1}}</td>
      
      

      
    </tr>
    <tr>
      <th scope="row">2</th>
      <td><input type="number" placeholder="0.00" @input="salary02 = $event.target.value" /></td>
      <td><input type="number" placeholder="0.00" @input="comission02 = $event.target.value"  /></td>
      <td>{{Total2}}</td>
    </tr>
    <tr>
      <th scope="row">3</th>
        <td><input type="number" placeholder="0.00" @input="salary03 = $event.target.value"  /></td>
        <td><input type="number" placeholder="0.00" @input="comission03 = $event.target.value"  /></td>
      <td>{{Total3}}</td>
    </tr>
    <tr>
      <th scope="row">4</th>
        <td><input type="number" placeholder="0.00" @input="salary04 = $event.target.value"  /></td>
        <td><input type="number" placeholder="0.00"  @input="comission04 = $event.target.value" /></td>
      <td>{{Total4}}</td>
    </tr>
    <tr>
      <th scope="row">5</th>
        <td><input type="number" placeholder="0.00" @input="salary05 = $event.target.value" /></td>
        <td><input type="number" placeholder="0.00" @input="comission05 = $event.target.value" /></td>
      <td>{{Total5}}</td>
    </tr>
    <tr>
      <th scope="row">6</th>
        <td><input type="number" placeholder="0.00" @input="salary06 = $event.target.value"  /></td>
        <td><input type="number" placeholder="0.00" @input="comission06 = $event.target.value" /></td>
      <td>{{Total6}}</td>
    </tr>
    <tr>
      <th scope="row">7</th>
        <td><input type="number" placeholder="0.00" @input="salary07 = $event.target.value" /></td>
        <td><input type="number" placeholder="0.00" @input="comission07 = $event.target.value" /></td>
      <td>{{Total7}}</td>
    </tr>
        <tr>
      <th scope="row">8</th>
        <td><input type="number" placeholder="0.00" @input="salary08 = $event.target.value" /></td>
        <td><input type="number" placeholder="0.00" @input="comission08 = $event.target.value" /></td>
      <td>{{Total8}}</td>
    </tr>
        <tr>
      <th scope="row">9</th>
        <td><input type="number" placeholder="0.00" @input="salary09 = $event.target.value" /></td>
        <td><input type="number" placeholder="0.00" @input="comission09 = $event.target.value" /></td>
      <td>{{Total9}}</td>
    </tr>
        <tr>
      <th scope="row">10</th>
        <td><input type="number" placeholder="0.00" @input="salary10 = $event.target.value" /></td>
        <td><input type="number" placeholder="0.00" @input="comission10 = $event.target.value" /></td>
      <td>{{Total10}}</td>
    </tr>
        <tr>
      <th scope="row">11</th>
        <td><input type="number" placeholder="0.00" @input="salary11 = $event.target.value" /></td>
        <td><input type="number" placeholder="0.00" @input="comission11 = $event.target.value" /></td>
      <td>{{Total11}}</td>
    </tr>
        <tr>
      <th scope="row">12</th>
        <td><input type="number" placeholder="0.00" @input="salary12 = $event.target.value" /></td>
        <td><input type="number" placeholder="0.00" @input="comission12 = $event.target.value" /></td>
      <td>{{Total12}}</td>
    </tr>
  </tbody>  
  </table>
   <button v-on:click="operacion()" class="btn btn-primary">Calculate</button>
 </div>

  
</div> 

  <p>Summary Total {{summaryTotal}}</p>
  <p>Salary Monthly {{promedioMensual}}</p>
  <p>Salary Diary{{promedioDiario}}</p>

  <p>preavisado{{preavisado}}</p>



</template>

<script>

export default {
  name: 'IngresarSalario',
  data() {
      return{
        Total1: null,
        Total2: null,
        Total3: null,
        Total4: null,
        Total5: null,
        Total6: null,
        Total7: null,
        Total8: null,
        Total9: null,
        Total10: null,
        Total11: null,
        Total12: null,
        salary01: 0,
        comission01: 0,
        salary02: 0,
        comission02: 0,
        salary03: 0,
        comission03: 0,
        salary04: 0,
        comission04: 0,
        salary05: 0,
        comission05: 0,
        salary06: 0,
        comission06: 0,
        salary07: 0,
        comission07: 0,
        salary08: 0,
        comission08: 0,
        salary09: 0,
        comission09: 0,
        salary10: 0,
        comission10: 0,
        salary11: 0,
        comission11: 0,
        salary12: 0,
        comission12: 0,
        
        summaryTotal: 0,
        promedioMensual: 0,
        promedioDiario: 0

         
      }

  },
  props:{

  },
 methods: {

   operacion: function(){

     this.Total1 = parseInt(this.salary01) + parseInt(this.comission01)
     this.Total2 = parseInt(this.salary02) + parseInt(this.comission02)
     this.Total3 = parseInt(this.salary03) + parseInt(this.comission03)
     this.Total4 = parseInt(this.salary04) + parseInt(this.comission04)
     this.Total5 = parseInt(this.salary05) + parseInt(this.comission05)
     this.Total6 = parseInt(this.salary06) + parseInt(this.comission06)
     this.Total7 = parseInt(this.salary07) + parseInt(this.comission07)
     this.Total8 = parseInt(this.salary08) + parseInt(this.comission08)
     this.Total9 = parseInt(this.salary09) + parseInt(this.comission09)
     this.Total10 = parseInt(this.salary10) + parseInt(this.comission10)
     this.Total11 = parseInt(this.salary11) + parseInt(this.comission11)
     this.Total12 = parseInt(this.salary12) + parseInt(this.comission12)

     this.summaryTotal = parseInt(this.salary01) + parseInt(this.comission01) + 
     parseInt(this.salary02) + parseInt(this.comission02) + parseInt(this.salary03) + 
     parseInt(this.comission03) + parseInt(this.salary04) + parseInt(this.comission04) +
     parseInt(this.salary05) + parseInt(this.comission05) +  parseInt(this.salary06) + 
     parseInt(this.comission06) + parseInt(this.salary07) + parseInt(this.comission07) +
     parseInt(this.salary08) + parseInt(this.comission08) +  parseInt(this.salary09) + 
     parseInt(this.comission09) +  parseInt(this.salary10) + parseInt(this.comission10) +
     parseInt(this.salary11) + parseInt(this.comission11) + parseInt(this.salary12) + 
     parseInt(this.comission12)

     this.promedioMensual = parseInt((this.summaryTotal) / (12))

     this.promedioDiario = parseInt((this.promedioMensual) / (23.83))

     this.preavisado = parseInt(this.summaryTotal) / (12)
     this.preavisado = parseInt(this.preavisado) / (23.83)






        

        
      


        


  





      }
   
 }




}
</script>

<style scoped>

.btn {
    padding: 0.5em 1em;
  border: none;
  cursor: pointer;
}

.btn {
    margin: 5px;
    padding: 0.5em 1em;
  border: none;
  cursor: pointer;
}

</style>
