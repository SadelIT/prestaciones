<template>
  <div class="datos">
    
  </div>

  <p>ID: {{ ID }}</p>
  <input v-model="ID" placeholder="Your ID" />

  <p>NAME: {{ Name }}</p>
  <input v-model="Name" placeholder="Your Name" />

  <p>COMPANY: {{ Company }}</p>
  <input v-model="Company" placeholder="Your Company" />

  
  
</template>

<script>
export default {
  name: 'IngresarDatos',
  data() {
    return {
      message: '',
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