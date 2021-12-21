<template>
  <div id="app">
    <Header @search="searching"/>
    <Main/>

  </div>
</template>

<script>
import axios from 'axios';
import Header from './components/macro/Header.vue';
import Main from './components/macro/Main.vue'

export default {
  name: 'App',
  components: {
      Header,
      Main
  },
  methods:{
    searching(payload){
      axios.get("https://api.themoviedb.org/3/search/movie", {
        params: {
          api_key: '047844b9c25649be8c8351e124316cf0',
          language: 'it_IT',
          query: payload
        }
      })
      .then((response) => {
        console.log(response)
      })
      .catch((error) => {
        console.log(error)
      });
    }
  }
}
</script>

<style lang="scss">

</style>
