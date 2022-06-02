<template>
<div>
<input type="number" :value="value0" @input="numberone = $event.target.value" >
<input type="number" :value="value1" @input="numbertwo = $event.target.value" >
<button v-on:click="operacion()">Resolver</button>
<p>Health Discounts: {{mensaje}}</p>
<p>Social Security Discounts: {{mensaje2}}</p>
<p>Taxes Discounts: {{mensaje3}}</p>
<p>Taxes Discounts: {{mensaje4}}</p>
<p>Discounts: {{mensaje5}}</p>
<p>Net Salary: {{mensaje5}}</p>
</div>

<<<<<<< HEAD
  

=======
  <p>ID: {{ ID }}</p>
  <input type="number" v-model="ID" placeholder="Your ID" />

  <p>NAME: {{ Name }}</p>
  <input type="text" v-model="Name" placeholder="Your Name" />

  <p>COMPANY: {{ Company }}</p>
  <input type="text" v-model="Company" placeholder="Your Company" />

  <h1>Seleccione La fecha de inicio y finalizacion laboral </h1>

<label for="start">Fecha de Inicio:</label>

<input type="date" id="inicio" name="trip-start"
       value=""
       min="" max="">


       <label for="start">Fecha de Salida:</label>

<input type="date" id="salida" name="trip-start"
       value=""
       min="" max="">


       <h1>Seleccione el período</h1>

<input type="radio" name="test" value="mensual"> Mnesual
<input type="radio" name="test" value="Quincenal"> Quincenal
<input type="radio" name="test" value="Semanal"> Semanal
<input type="radio" name="test" value="Diario"> Diario


<h1>Seleccione el tipo de calculo </h1>

<input type="radio" name="test" value="Ordinario"> Ordinario
<input type="radio" name="test" value="Intermitente"> Intermitente

<p>Jornada ordinaria es la ejecutada por trabajadores dentro de un período que no exceda de ocho (8) horas al día ni de cuarenta y cuatro (44) a la semana.</p>
>>>>>>> 29a6e1132f7f49e858ee90ea03bedca91f7f9f5b

  
  
</template>

<script>
  
  export default {
  
  
  name: 'IngresarDatos',
<<<<<<< HEAD
  data: function () {
        return {
            numberone: null,
            numbertwo: null,
            mensaje: null,
            mensaje2: null,
            mensaje3: null
        }
    },
    methods: {
        operacion() {
            this.mensaje = parseInt(this.numberone) +
                parseInt(this.numbertwo);
            this.mensaje2 = parseInt(this.numberone) -
                parseInt(this.numbertwo);
            this.mensaje3 = parseInt(this.numberone) *
                parseInt(this.numbertwo);
        }
    },
=======
  data() {
    return {
      ID: '',
      Name: '',
      Company: ''

    }
  },
  props: {
    msg: String
  }
>>>>>>> 29a6e1132f7f49e858ee90ea03bedca91f7f9f5b
}
</script>