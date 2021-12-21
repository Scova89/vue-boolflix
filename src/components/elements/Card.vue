<template>
    <div>
        <h3>{{info.title}}</h3>
        <h4>{{info.original_title}}</h4>
        <p>{{info.original_language}}</p>
        <p>{{info.vote_average}}</p>
    </div>
     
</template>

<script>
export default {
    name:'Card',
    props: {
        info: Object
    }
}
</script>

<style>

</style>