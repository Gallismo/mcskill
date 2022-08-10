<template>
    <div id="search" class="flex-grow-1">
        <div class="input-group mb-3" id="search-container">
            <search-icon/>

            <input type="text" class="form-control" id="search-input" placeholder="Поиск товара по названию"
                   aria-label="search" v-model="search" @input="searchItems">
        </div>
    </div>
</template>

<script>
    import SearchIcon from "@/components/ServerStore/icons/SearchIcon";
    export default {
        name: "Search",
        components: {SearchIcon},
        data() {
            return {
                search: ''
            }
        },
        methods: {
            searchItems() {
                this.$store.dispatch('searchItem', this.search)
            }
        }
    }
</script>

<style scoped>

</style>