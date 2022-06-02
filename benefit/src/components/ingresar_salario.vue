<template>

<div></div>
<!--
<button  class="btn btn-primary" @click="click('calculate')">calculate</button>

<button  class="btn btn-danger" @click="click('reset')">reset</button>




<p class="text-lowercase">{{GrossSalary}}</p>

<p class="text-lowercase">{{HealthDiscounts}}</p>
<p class="text-lowercase">{{HealthDiscounts}}</p>

<p class="text-lowercase">{{TaxesDiscounts}}:</p>
<p class="text-lowercase">{{Discounts}}</p>
<p class="text-lowercase">{{NetSalary}}</p>

<div id="app">
 Type the first number:
 <input type="number" v-model.number="n1"><br />
 Type the second number:
 <input type="number" v-model.number="n2"><br />
 The sum() is: {{ sum() }}<br />
 The sum2 is: {{ sum2 }} <br>
 the number  is: {{ sum3 }}
</div>

-->




  
</template>

<script>
export default {
  name: 'IngresarSalario',
  data() {
      return{
          n1: 0,
          n2: 0
      }

  },
  computed: {
   sum2: function () {
     console.log('prop-> ' + this.n1 + '+' + this.n2);
     return this.n1 + this.n2;
   }
 },
 methods: {
   sum: function () {
     console.log('method-> ' + this.n1 + '+' + this.n2);
     return this.n1 + this.n2;
   }
 }




}
</script>