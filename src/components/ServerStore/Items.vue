<template>
    <div id="items" class="grid-4 grid-gap-2">
        <add-item-card/>

        <item-card v-for="item in allItems" :item="item"/>
    </div>
</template>

<script>
    import AddItemCard from "@/components/ServerStore/cards/AddItemCard";
    import ItemCard from "@/components/ServerStore/cards/ItemCard";
    import {mapGetters} from "vuex";
    export default {
        name: "Items",
        components: {ItemCard, AddItemCard},
        computed: {
            ...mapGetters(['allItems'])
        }
    }
</script>

<style scoped>

</style>