<template>


  <div>
  <input type="number" :value="value0" @input="salary = $event.target.value" >


  <button v-on:click="operacion()">Resolver</button>

  <p>Salary: {{Salary1}}</p>
  <p>Health Discounts: {{Health}}</p>
  <p>Social Security Discounts: {{Social}}</p>
  <p>Taxes Discounts: {{Taxes}}</p>
  <p>Discounts: {{Discounts}}</p>
  <p>Net Salary: {{NetSalary}}</p>
  </div>

  
  
</template>

<script>
export default {
  name: 'IngresarDatos',
  data: function () {
        return {
            salary: null,
            Health: null,
            Social: null,
            Taxes: null,
            Discounts: null,
            NetSalary: null,
            isr: 0.15
        }
    },
    methods: {
        operacion() {
            
            this.Salary1 = (this.salary)
            
            this.Health = parseInt(this.salary) *
                (3.04 / 100);
                
            this.Social = parseInt(this.salary) *
                (2.87 / 100)

            this.Discounts = parseInt(this.Health) +
                parseInt(this.Social);

            this.NetSalary = parseInt(this.salary) -
                (this.Discounts);
            

           if (this.salary <= 55291.01  || this.salary >= 36862.01 ){
              this.Taxes =  this.NetSalary * this.isr
              
              
           } 
            else if(this.salary >= 55291.02){
                this.Taxes = 'hello'

            }

           //this.Taxes = parseInt(this.Taxes * this.isr)


            
            //if (this.salary >= 34685.01){
            //this.Taxes = (this.salary) * (12)
  
          //} 
          //this.Discounts = parseInt(this.Discounts) +
            //Math.round(this.Taxes)
           //this.NetSalary = parseInt(this.salary) -
                //Math.round(this.Discounts)
          
          
        }
    }
}
</script>