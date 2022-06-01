<template>
  <div class="datos">
    
  </div>

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

  
  
</template>

<script>
export default {
  name: 'IngresarDatos',
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
}
</script>