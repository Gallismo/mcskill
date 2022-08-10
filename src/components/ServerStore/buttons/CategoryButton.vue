<template>
    <button class="category" :data-id="category.id" @click="$emit('clickButton', category.id)">{{category.name}}</button>
</template>

<script>
    export default {
        name: "CategoryButton",
        props: {
            category: {
                type: Object,
                required: true
            }
        }
    }
</script>

<style scoped>

</style>