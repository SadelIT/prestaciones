<template>

<div></div>


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