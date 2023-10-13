<script>
import { store } from '../data/store'
import CardContainer from './CardContainer.vue';

export default {
  name : "Main",

  components : {
    CardContainer,
  },

  data () {
    return {
      store
    }
  }
}
</script>

<template>

  <div class="container">
    <select class="form-select" aria-label="Default select example">
      <option selected>Open this select menu</option>
      <option value="1">One</option>
      <option value="2">Two</option>
      <option value="3">Three</option>
    </select>

    <CardContainer />

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