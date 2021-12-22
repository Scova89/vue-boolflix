<template>
    <div>
        <h3>{{info.title}}</h3>
        <h4>{{info.original_title}}</h4>
        <div>
            <img v-if="flags.includes(info.original_language)" :src="require(`../../assets/flags/${info.original_language}.png`)" :alt="info.original_language" height="30">
            <img v-else src="../../assets/flags/rainbow-flag-2060.png" alt="flag not available" height="30">
        </div>
        <p>{{info.vote_average}}</p>
        <h2>{{info.popularity}}</h2>
    </div>
     
</template>

<script>
export default {
    name:'Card',
    props: {
        info: Object
    },
    data(){
        return {
            flags:['fr', 'it', 'en']
        }
    }
}
</script>

<style>

</style>