<template>
  <Ingresardatos></Ingresardatos>

  <seleccionarfecha></seleccionarfecha>

  <Seleccionarperiodo></Seleccionarperiodo>

  <Seleccionarcalculo></Seleccionarcalculo>

  <Ingresarsalario></IngresarSalario>

  <Seleccionarprestaciones></Seleccionarprestaciones>
  
  <Resumensalario></Resumensalario>

  
 
 
  


</template>

<script>
import Ingresardatos from './components/ingresar_datos.vue'
import Ingresarsalario from './components/ingresar_salario'
import Seleccionarprestaciones from './components/prestaciones'
import Resumensalario from './components/resumen_salarios'
import Seleccionarcalculo from './components/seleccionar_calculo'
import Seleccionarfecha from './components/seleccionar_fecha'
import Seleccionarperiodo from './components/seleccionar_periodo'


export default {

  
  name: 'App',
  components: {
    
    Ingresardatos,
    Ingresarsalario,
    Seleccionarprestaciones,
    Resumensalario,
    Seleccionarcalculo,
    Seleccionarfecha,
    Seleccionarperiodo
  }
}
</script>



<style>

</style>
