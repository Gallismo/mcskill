<template>
    <div id="store-sales" class="grid-4 grid-gap-3 text-center mb-2">
        <sale-button v-for="button in buttons" :data="button"/>
    </div>
</template>

<script>
    import SaleButton from "@/components/ServerStore/buttons/SaleButton";
    export default {
        name: "StoreSales",
        components: {SaleButton},
        data() {
            return {
                buttons: [
                    {title: "Привилегии", active: false},
                    {title: "Кейсы", active: false},
                    {title: "Предметы", active: true},
                    {title: "Наборы", active: false},
                ]
            }
        }
    }
</script>

<style scoped>

</style>