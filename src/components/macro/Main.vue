<template>
    <main>
        <FilmList/>
    </main>
</template>

<script>
import FilmList from '../sections/FilmList.vue';
import axios from 'axios';

export default {
    name: 'Main',
    components: {
      FilmList
  }
}
</script>

<style>

</style>