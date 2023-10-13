<script>

import Card from './partials/Card.vue';

export default {
  name: 'CardContainer',

  data () {
    return {
      Card
    }
  }
}
</script>


<template>

  <div class="container">
    <Card />
    <Card />
    <Card />
  </div>

</template>


<style scoped>

.container {
  background-color: white;
  height: 100px;
}

</style>