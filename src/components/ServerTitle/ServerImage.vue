<template>
    <div id="server_image">
        <img src="src/server_image.png" alt="">
        <server-change-button/>
    </div>
</template>

<script>
    import ServerChangeButton from "@/components/ServerTitle/ServerChangeButton";
    export default {
        name: "ServerImage",
        components: {ServerChangeButton}
    }
</script>

<style scoped>

</style>