<template>
  <section>
      <ul>
          <li v-for="(film, index) in films" :key="index">
              <h3>{{film.title}}</h3>
              <h4>{{film.original_title}}</h4>
              <p>{{film.original_language}}</p>
              <p>{{film.vote_average}}</p>

          </li>
      </ul>
  </section>
</template>

<script>
export default {
    name: 'FilmList',
    props: {
      films: Array
  }
}
</script>

<style>

</style>