<template>
  <div id="app">
    <Header @search="searching"/>
    <Main :series="series" :films="films"/>

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
  data(){
    return{
      films: [],
      series: []
    }
  },
  methods: {
    searching(payload) {
      // movies
      axios.get("https://api.themoviedb.org/3/search/movie", {
        params: {
          api_key: '047844b9c25649be8c8351e124316cf0',
          language: 'it_IT',
          query: payload,
        }
      })
      .then((response) => {
        this.films=response.data.results;
      })
      .catch((error) => {
        console.log(error)
      });
      // Tv series
      axios.get("https://api.themoviedb.org/3/search/tv", {
        params: {
          api_key: '047844b9c25649be8c8351e124316cf0',
          language: 'it_IT',
          query: payload,
        }
      })
      .then((response) => {
        this.series=response.data.results;
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
