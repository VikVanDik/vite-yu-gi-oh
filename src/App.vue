<script>
import Select from './components/Select.vue';
import Header from './components/Header.vue';
import { store } from './data/store';
import CardContainer from './components/CardContainer.vue';
import axios from 'axios';



export default {
  name : "App",

  components : {
    Select,
    Header,
    CardContainer
  },

  data () {
    return {
      store,
    }
  },

  methods : {
    getApi(){
      axios.get(store.apiUrl, {
        params : {
          num : 50,
          offset: 0,
          archetype: ''
        }
      })

      .then (res => {
        store.cardsList = res.data.data
      })
    },

    getFullApi (){
      axios.get(store.apiUrl)

      .then (res=> {
        store.cardsListAll = res.data.data
        

        store.cardsListAll.forEach(cardType => {
          if (!store.archetypeList.includes(cardType.archetype)){
            store.archetypeList.push(cardType.archetype)
          }
        })
        console.log(store.archetypeList);
      })
    }
  },
  mounted (){
    this.getApi()
    this.getFullApi()
  }

}
</script>

<template>
  <div>
    <Header />
    <Select />
    <CardContainer />

  </div>
  
</template>

<style lang="scss">

@use './scss/main.scss';

</style>
