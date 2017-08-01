<template>
    <v-container fluid>
        <v-layout row wrap>
            <v-flex md2>
                <v-switch label="Home" v-model="switch_home"></v-switch>
            </v-flex>
            <v-flex md5>
                <v-text-field name="home_url" label="Url" id="testing"></v-text-field>
            </v-flex>
            <v-flex md5>
                <v-text-field name="home_identifiant" label="Identifiant" id="testing"></v-text-field>
            </v-flex>
        </v-layout>
        <v-layout row wrap>
            <v-flex md2>
                <v-switch label="Category" v-model="switch_category"></v-switch>
            </v-flex>
            <v-flex md5>
                <v-text-field name="category_url" label="Url" id="testing"></v-text-field>
            </v-flex>
            <v-flex md5>
                <v-text-field name="category_identifiant" label="Identifiant" id="testing"></v-text-field>
            </v-flex>
        </v-layout>
        <v-layout row wrap>
            <v-flex md2>
                <v-switch label="Listing" v-model="switch_listing"></v-switch>
            </v-flex>
            <v-flex md5>
                <v-text-field name="listing_url" label="Url" id="testing"></v-text-field>
            </v-flex>
            <v-flex md5>
                <v-text-field name="listing_identifiant" label="Identifiant" id="testing"></v-text-field>
            </v-flex>
        </v-layout>
        <v-layout row wrap>
            <v-flex md2>
                <v-switch label="Offer" v-model="switch_offer"></v-switch>
            </v-flex>
            <v-flex md5>
                <v-text-field name="offer_url" label="Url" id="testing"></v-text-field>
            </v-flex>
            <v-flex md5>
                <v-text-field name="offer_identifiant" label="Identifiant" id="testing"></v-text-field>
            </v-flex>
        </v-layout>
    </v-container>
</template>

<script>
    export default {
        data() {
            return {
                switch_home: false,
                switch_category: false,
                switch_listing: false,
                switch_offer: true,
            }
        }
    }
</script>
