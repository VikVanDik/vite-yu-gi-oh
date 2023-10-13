<script>
import Card from './partials/Card.vue'


export default {
  name: 'CardContainer',

  components : {
    Card
  },

  data () {
    return {
      Card
    }
  }
}
</script>


<template>

  <div class="container cardContainer row justify-content-center ">
    <Card />
    <Card />
    <Card />
    <Card />
    <Card />
    <Card />
    <Card />
    <Card />
    
  </div>

</template>


<style scoped>

.cardContainer {
  background-color: white;
  
  
}

</style>