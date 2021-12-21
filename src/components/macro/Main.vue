<template>
    <main>
        <FilmList/>
    </main>
</template>

<script>
import FilmList from '../sections/FilmList.vue';


export default {
    name: 'Main',
    components: {
      FilmList
  },
  props: {
      films: Array
  }
}
</script>

<style>

</style>