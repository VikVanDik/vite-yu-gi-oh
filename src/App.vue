<script>
import Main from './components/Main.vue';
import Header from './components/Header.vue';
import { store } from './data/store';



export default {
  name : "App",

  components : {
    Main,
    Header,
  },

  data () {
    return {
      store,
    }
  }
}
</script>

<template>
  <div>
    <Header />
    <Main />

  </div>
  
</template>

<style lang="scss">

@use './scss/main.scss';

</style>
