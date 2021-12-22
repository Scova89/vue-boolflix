<template>
    <main>
        <FilmList :films="films"/>
        <SerieList :series="series"/>
    </main>
</template>

<script>
import FilmList from '../sections/FilmList.vue';
import SerieList from '../sections/SerieList.vue';


export default {
    name: 'Main',
    components: {
      FilmList,
      SerieList
  },
  props: {
      films: Array,
      series: Array
  }
}
</script>

<style>

</style>