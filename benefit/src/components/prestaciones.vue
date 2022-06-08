<template>

  <div>

  <input type="checkbox"  v-model="preAvisado" /> pre-notified?
	<label for="checkbox">{{  }}</label>

  <input type="checkbox"  v-model="fortnightly" /> include unemployment?
	<label for="checkbox">{{  }}</label>

  <input type="checkbox"  v-model="weekly" /> You have taken vacation?
	<label for="checkbox">{{  }}</label>

  <input type="checkbox"  v-model="diary" /> Include Christmas bonus?
	<label for="checkbox">{{  }}</label>
  
  </div>

  
</template>

<script>
export default {
  name: 'SeleccionarPrestaciones',
  data() {
    return {


    }
  }

}
</script>