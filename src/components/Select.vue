<script>
import { store } from '../data/store'



export default {
  name : "Select",

 

  data () {
    return {
      store
    }
  }
}
</script>

<template>

  <div class="container">
    <select class="form-select" aria-label="Default select example" >
      <option selected>Seleziona l'archetipo</option>
      <option 
      v-for="(archetype, index) in store.archetypeList" 
      :key ="index"
      >{{ archetype }}</option>
      
    </select>
  </div>
  
</template>

<style lang="scss" scoped>
.container {
  select {
    width: 300px;
    margin-block: 50px;
  }
}

</style>