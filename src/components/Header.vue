<script>


export default {
  name : "Header"

}
</script>

<template>
  
  <header class="d-flex align-items-center ">
    <img src="/public/YuGiOh.webp" alt="">
    <div>Yu-Gi-Oh API</div>
  </header>
  
</template>

<style lang="scss" scoped>



header {
  height: 50px;
  background-color: red;
  img {
    width: 100px;
  }
  div {
    font-size: 35px;
  }

}
</style>