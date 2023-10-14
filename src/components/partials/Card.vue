<script>
export default {
  name : 'Card',
  props:{
    nameStr: String,
    archetypeStr: String,
    imgStr: String,
  }

}

</script>

<template>
  
  <div class="cardYu col-2 d-flex flex-column align-items-center">
    <img :src="imgStr" alt="">
    <div v-if="archetypeStr">{{ archetypeStr }}</div>
    <div v-else> - </div>
    <div>{{ nameStr }}</div>
  </div>
  
</template>

<style lang="scss" scoped>
  .cardYu {
    margin: 10px;
    width: 150px;
    height: 300px;
    background-color: #D48F38;
    img {
      width: 150px;
    }
  }

</style>