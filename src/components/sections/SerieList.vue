<template>
  <section>
      <h1>TV Series</h1>
      <ul>
          <li v-for="(serie, index) in series" :key="index">
              <Card :info="serie"/>
          </li>
          
      </ul>
  </section>
</template>

<script>
import Card from '../elements/Card.vue';
export default {
    name: "SerieList",
    props: {
        series: Array
    },
    components: {
        Card
    }
}
</script>

<style>

</style>