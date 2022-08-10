<template>
    <div id="store">
        <store-sales/>
        <div class="d-flex mb-2">
            <search/>
            <Filter/>
        </div>
        <div class="row">
            <categories/>
            <items/>
        </div>
    </div>
</template>

<script>
    import StoreSales from "@/components/ServerStore/StoreSales";
    import Search from "@/components/ServerStore/Search";
    import Filter from "@/components/ServerStore/Filter";
    import Categories from "@/components/ServerStore/Categories";
    import Items from "@/components/ServerStore/Items";
    export default {
        name: "ServerStore",
        components: {Items, Categories, Filter, Search, StoreSales}
    }
</script>

<style scoped>

</style>