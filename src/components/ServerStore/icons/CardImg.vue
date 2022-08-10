<template>
    <div class="card-img-top">
        <div class="item-icon-container">
            <img class="item-icon" :src="url" alt="">
        </div>
    </div>
</template>

<script>
    export default {
        name: "CardImg",
        props: {
            url: {
                type: String,
                required: true
            }
        }
    }
</script>

<style scoped>

</style>