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

  


  
  
</template>

<script>
  
  export default {
  
  
  name: 'IngresarDatos',
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
}
</script>