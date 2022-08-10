<template>
    <div id="categories">
        <div id="open_cats" @click="switchVisible">
            <div>Категории</div>
        </div>
        <div id="cats-list" class="grid-5 grid-gap-1" :class="{'show-grid': opened, 'hidden': !opened}">
            <category-button :category="{name:'Все товары', id:0}" @clickButton="clearCats"/>
            <category-button v-for="category in allCategories" :category="category" @clickButton="selectCat"/>
        </div>
    </div>
</template>

<script>
    import CategoryButton from "@/components/ServerStore/buttons/CategoryButton";
    import {mapGetters, mapActions} from 'vuex';
    export default {
        name: "Categories",
        components: {CategoryButton},
        methods: {
            ...mapActions(['clearSelected', 'selectCategory']),
            switchVisible() {
                const cats = document.getElementById('cats-list');
                switch (cats.classList.contains("hidden")) {
                    case true:
                        cats.classList.remove("hidden");
                        cats.classList.add("show-grid");
                        break;
                    case false:
                        cats.classList.remove("show-grid");
                        cats.classList.add("hidden");
                        break;
                }
            },
            clearCats() {
                this.clearSelected();
            },
            selectCat(id) {
                this.selectCategory(id);
            }
        },
        data() {
            return {
                opened: false
            }
        },
        computed: {
            ...mapGetters(["allCategories"])
        }
    }
</script>

<style scoped>

</style>