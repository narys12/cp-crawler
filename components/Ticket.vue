<template>
    <v-card flat>
        <v-card-text>
            <v-container fluid>
                <v-layout row wrap>
                    <v-flex>
                        <v-select 
                            v-bind:items="site_types" 
                            v-model="siteType" 
                            class="pr-4"
                            label="Type du site"></v-select>
                    </v-flex>
                    <v-flex>
                        <v-select 
                            v-bind:items="variantes" 
                            v-model="variante" 
                            class="pr-4"
                            label="Variantes" 
                            multiple></v-select>
                    </v-flex>
                    <v-flex>
                        <v-select 
                            v-bind:items="pages" 
                            v-model="page" 
                            label="Pages crawlables" 
                            multiple></v-select>
                    </v-flex>
                </v-layout>
                <v-layout row wrap>
                    <v-data-table
                        v-bind:headers="pages"
                        :items="pages_identifiers"
                        hide-actions
                        class="elevation-1"
                    >
                        <template slot="pages_identifiers" scope="props">
                            <td>Pages crawlables</td>
                            <td class="text-xs-right">{{ props.item.home }}</td>
                            <td class="text-xs-right">{{ props.item.category }}</td>
                            <td class="text-xs-right">{{ props.item.listing }}</td>
                            <td class="text-xs-right">{{ props.item.offer }}</td>
                        </template>
                    </v-data-table>
                </v-layout>
            </v-container>
        </v-card-text>
    </v-card>
</template>

<script>
    export default {
        data() {
            return {
                siteType: null,
                variante: null,
                page: null,
                site_types: [
                    {text: "Standard"},
                    {text: "MarketPlace"}
                ],
                variantes: [
                    {text: "couleur"},
                    {text: "taille"}
                ],
                pages: [
                    {text: "Pages", value:"name"},
                    {text: "Home", value:"home"},
                    {text: "Category", value: "category"},
                    {text: "Listing", value: "listing"},
                    {text: "Offer", value: "offer"}
                ],
                pages_identifiers: [
                    {value: false},
                    {home: "x"},
                    {category: "x"},
                    {listing: "x"},
                    {offer: "x"}
                ]
            }
        }
    }
</script>