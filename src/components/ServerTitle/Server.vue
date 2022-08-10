<template>
    <server-title/>
    <hr>
    <server-image/>
    <hr>
</template>

<script>
    import ServerTitle from "@/components/ServerTitle/ServerTitle";
    import ServerImage from "@/components/ServerTitle/ServerImage";
    export default {
        name: "Server",
        components: {ServerImage, ServerTitle}
    }
</script>

<style scoped>

</style>