<template>
    <v-container>
        <v-layout wrap>
            <v-flex md2>
            </v-flex>
            <v-flex md8>
                    <v-text-field
                        name="input-1"
                        label="Url du site"
                        id="testing"
                    ></v-text-field>
                
            </v-flex>
            <v-flex md2>
            </v-flex>
        </v-layout>
    </v-container>
</template>

<script>
    export default {
        data() {
            return {
                home: null,
                category: null,
                listing: null,
                offer: null,
            }
        }
    }
</script>