<template>
<h1>Seleccione La fecha de inicio y finalizacion laboral </h1>

<label for="start">Fecha de Inicio:</label>

<input type="date" id="inicio" name="trip-start"
       value=""
       min="" max="">


       <label for="start">Fecha de Salida:</label>

<input type="date" id="salida" name="trip-start"
       value=""
       min="" max="">


  
  
</template>

<script>
export default {
  name: 'SeleccionarFecha',
  data() {
    return {
        


    }
  }

}
</script>