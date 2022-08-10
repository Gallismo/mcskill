<template>
    <p class="card-text price-container">
        <span class="price">{{value}}</span>
        <img src="src/ruble-icon.svg" alt="" class="price-icon" v-if="rub">
        <img src="src/emerald-icon.svg" alt="" class="price-icon" v-else>
    </p>
</template>

<script>
    export default {
        name: "ItemPrice",
        props: {
            value: {
                type: String,
                required: true
            },
            rub: {
                type: String,
                required: true
            }
        }
    }
</script>

<style scoped>

</style>