<template>
    <back-arrow/>
    <server/>
    <server-store/>
</template>

<script>
    import BackArrow from "@/components/BackArrow";
    import Server from "@/components/ServerTitle/Server";
    import ServerStore from "@/components/ServerStore/ServerStore";
    export default {
        name: "Store",
        components: {ServerStore, Server, BackArrow}
    }
</script>

<style scoped>

</style>