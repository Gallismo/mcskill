<template>
    <button class="sale-button" :class="{selected:data.active}">{{data.title}}</button>
</template>

<script>
    export default {
        name: "SaleButton",
        props: {
            data: {
                type: Object,
                required: true
            }
        }
    }
</script>

<style scoped>

</style>