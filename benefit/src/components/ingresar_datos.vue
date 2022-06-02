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
            NetSalary: null
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

            this.Taxes = parseInt(this.salary) -
             parseInt(this.Discounts)

            

            //if (this.salary >= 416220.01 / 12  || this.salary == 624329.00){
            //this.Taxes = (this.NetSalary) * (0.15 / 100)

          //} 

          //this.Discounts = parseInt(this.Discounts) +
            //Math.round(this.Taxes)

           //this.NetSalary = parseInt(this.salary) -
                //Math.round(this.Discounts)
          

          
        }
    }
}
</script>