<template>
    <div class="card item" :data-id="item.id">
        <card-img :url="item.img"/>
        <div class="card-body">
            <h5 class="card-title">{{item.name}}</h5>

            <button class="btn buy-button">Купить</button>

            <item-price v-if="parseFloat(item.pricerub) > 0" :value="item.pricerub" :rub="true"/>
            <item-price v-if="parseFloat(item.priceem) > 0" :value="item.priceem" :rub="false"/>
        </div>
        <div class="item-buttons">
            <edit-button/>
            <delete-button/>
        </div>
    </div>
</template>

<script>
    import CardImg from "@/components/ServerStore/icons/CardImg";
    import ItemPrice from "@/components/ServerStore/ItemPrice";
    import EditButton from "@/components/ServerStore/buttons/EditButton";
    import DeleteButton from "@/components/ServerStore/buttons/DeleteButton";
    export default {
        name: "ItemCard",
        components: {DeleteButton, EditButton, ItemPrice, CardImg},
        props: {
            item: {
                type: Object,
                required: true
            }
        }
    }
</script>

<style scoped>

</style>