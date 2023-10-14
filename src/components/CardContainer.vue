<script>
import Card from './partials/Card.vue'
import { store } from '../data/store'


export default {
  name: 'CardContainer',

  components : {
    Card
  },

  data () {
    return {
      Card,
      store,
    }
  }
}
</script>


<template>

  <div class="container">
    <div class=" cardContainer row justify-content-center ">
      <Card 
      v-for = "card in store.cardsList" 
      :key = "card.id" 
      :nameStr="card.name"
      :archetypeStr="card.archetype"
      :imgStr="card.card_images[0].image_url"/>
      
    </div>
    
  </div>

</template>


<style scoped>

.cardContainer {
  background-color: white;
}

</style>