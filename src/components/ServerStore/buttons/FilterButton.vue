<template>
    <button class="dropdown-item">
        <img :src="data.img" alt="">
        <span class="text">{{data.text}}</span>
    </button>
</template>

<script>
    export default {
        name: "FilterButton",
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