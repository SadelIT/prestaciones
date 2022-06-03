 <template>

    <div class="card"  id="Calculo">
    <div class="container">

    <p>Enter your salary </p>

    <p> 
    <input class="inpu" type="number" :value="vlaue0"  @input="salary = $event.target.value" >
    </p>

  

        <p>Salary: {{Salary1}}</p>
        <p>Health Discounts: {{Health}}</p>
        <p>Social Security Discounts: {{Social}}</p>
    
        <p>Taxes Discounts monthly: {{Taxes}}</p>
  
  
        <p>Discounts: {{Discounts}}</p>
        <p>Net Salary: {{NetSalary}}</p>

        <div class="control">
        <p>
        <button v-on:click="operacion()" class="btnC">Calculate</button>
        
        <button @click="reset" class="btnR">Reset</button> 
        </p>
        </div>

        
    </div>
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
            AnnualSalary: null
        }
    },
    methods: {
        reset() {
       this.Salary1 = '',
       this.Health = '',
       this.Social = '',
       this.Taxes = '',
       this.Discounts = '',
       this.NetSalary = '',
       this.AnnualSalary = ''
    },
        
        operacion: function() {
            



            this.Salary1 = (this.salary)
            
            this.Health = parseInt(this.salary) *
                (3.04 / 100);
                
            this.Social = parseInt(this.salary) *
                (2.87 / 100)



            this.Discounts = parseInt(this.Health) +
                parseInt(this.Social);

            this.NetSalary = parseInt(this.salary) -
                (this.Discounts);
             
            this.AnnualSalary = parseInt(this.NetSalary) * (12).toFixed(1)



            if ( this.AnnualSalary >= 416220.01){
            this.Taxes = parseInt(this.AnnualSalary) -  (416220)

            
              this.Taxes = (this.Taxes) *  (0.15)
              this.Taxes = ((this.Taxes) /  (12)).toFixed(2)

                 console.log(this.Taxes)
                if( this.AnnualSalary >= 624329.01){
                this.Taxes = (this.AnnualSalary) - (624329)

            
                this.Taxes = (this.Taxes) *  (0.20) + (2601.33)
                this.Taxes = ((this.Taxes) /  (12)).toFixed(2)

                console.log(this.Taxes)
                }

                if( this.AnnualSalary >= 867123.01){
                this.Taxes = (this.AnnualSalary) -  (867123)

            
                this.Taxes = (this.Taxes) *  (0.25) + (6648)
                this.Taxes = ((this.Taxes) /  (12)).toFixed(2)

                console.log(this.Taxes)
                }



             this.Discounts = parseInt(this.Discounts) + parseInt(this.Taxes)  

             this.NetSalary = parseInt(this.salary) - parseInt(this.Discounts)


            } 

            
            ///else if( this.AnnualSalary >= 624329.01){
            //this.Taxes = (this.AnnualSalary) - (416220)

            
            //this.Taxes = (this.Taxes) *  (0.20)
            //this.Taxes = (this.Taxes) /  (12)

            //console.log(this.Taxes + 'im')
            //}
            
            //else if (this.AnnualSalary > 624329.01){
              //  this.Taxes = 'hello'

             // }




            



          //this.Discounts = parseInt(this.Discounts) +
            //(this.Taxes)

           //this.NetSalary = parseInt(this.salary) -
                //(this.Discounts)
          
        
          
        }
        
    }
}
</script>



<style scoped>

.card {
 
  box-shadow: 0 4px 8px 0 rgba(0,0,0,0.2);
  transition: 0.3s;
  margin: 300px;
  margin-top: 0;
  align: center
}


.card:hover {
  box-shadow: 0 8px 16px 0 rgba(0,0,0,0.2);
}


.container {
    
  
  

}

p {
  text-align: center;
}



.btnC {
    padding: 0.5em 1em;
  border: none;
  background: rgb(100, 200, 255);
  cursor: pointer;
}

.btnR {
    margin: 5px;
    padding: 0.5em 1em;
  border: none;
  background: rgb(255,0,0);
  cursor: pointer;
}

</style>