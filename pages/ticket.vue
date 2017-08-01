<template>
    <v-tabs dark v-model="active">
        <v-tabs-bar slot="activators" class="cyan">
            <v-tabs-item v-for="tab in tabs" :key="tab" :href="'#' + tab" ripple>
                {{ tab }}
            </v-tabs-item>
            <v-tabs-slider class="yellow"></v-tabs-slider>
        </v-tabs-bar>
        <v-tabs-content v-for="tab in tabs" :key="tab" :id="tab">
            <v-card v-if="tab==='Pages'">
                <Pages/>
            </v-card>
            <v-card v-if="tab==='Discoveries'">
                <Discoveries/>
            </v-card>
            <v-card v-if="tab==='Product'">
                <Product/>
            </v-card>
            <v-card v-if="tab==='Offer Specifications'">
                <Offer/>
            </v-card>
        </v-tabs-content>
    </v-tabs>
</template>

<script>
    import Pages from "../components/Pages"
    import Discoveries from "../components/Discoveries"
    import Product from "../components/Product"
    import Offer from "../components/Offer"

    export default {
        data() {
            return {
                tabs: ['Pages', 'Discoveries', 'Product', 'Offer Specifications'],
                active: null,
            }
        },
        components: {
            Pages,
            Discoveries,
            Product,
            Offer
        }
    }
</script>

<style lang="css" scoped>

</style>