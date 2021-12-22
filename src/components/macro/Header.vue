<template>
    <header>
        <div class="search-bar" @submit.prevent="$emit('search', textToSearch)">
            <form action="">
                <input v-model="textToSearch" type="text">
                <button>Search</button>
            </form>
            
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