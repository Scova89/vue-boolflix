<template>
  <section>
      <h1>Movies</h1>
      <ul>
          <li v-for="(film, index) in films" :key="index">
              <Card :info="film"/>
          </li>
          
      </ul>
  </section>
</template>

<script>
import Card from '../elements/Card.vue';
export default {
  name: 'FilmList',
  props: {
      films: Array,
      series: Array
  },
  components: {
      Card
  }
}
</script>

<style>

</style>