<template>
    <header>
        <div class="search-bar">
            <input v-model="textToSearch" type="text">
            <button>Search</button>
        </div>
    </header>
</template>

<script>
export default {
    name: 'Header',
    data() {
        return {
            textToSearch: ""
        }
    }
}
</script>

<style>

</style>