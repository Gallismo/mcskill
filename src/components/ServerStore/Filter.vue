<template>
    <div class="flex-shrink-1" id="filter">
        <filter-icon/>
        <div id="filters">
            <filter-button v-for="filter in filters" :data="filter"/>
        </div>
    </div>
</template>

<script>
    import FilterIcon from "@/components/ServerStore/icons/FilterIcon";
    import FilterButton from "@/components/ServerStore/buttons/FilterButton";
    export default {
        name: "Filter",
        components: {FilterButton, FilterIcon},
        data() {
            return {
                filters: [
                    {img: "src/filter-1.svg", text: "По алфавиту"},
                    {img: "src/filter-2.svg", text: "По алфавиту"},
                    {img: "src/filter-3.svg", text: "По цене"},
                    {img: "src/filter-4.svg", text: "По цене"}
                ]
            }
        }
    }
</script>

<style scoped>

</style>