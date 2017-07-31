<template>
  <v-app toolbar footer>
    <v-tabs dark v-model="active">
      <v-tabs-bar slot="activators" class="cyan">
        <v-tabs-item
          v-for="tab in tabs"
          :key="tab"
          :href="'#' + tab"
          ripple
        >
          {{tab}}
        </v-tabs-item>
        <v-tabs-slider class="yellow"></v-tabs-slider>
      </v-tabs-bar>
      <v-tabs-content :id="tabs[0]">
        <Ticket></Ticket>
      </v-tabs-content>
      <v-tabs-content :id="tabs[1]">
        <Crawler></Crawler>
      </v-tabs-content>
    </v-tabs>
  </v-app>
</template>

<script>
  import Ticket from '../components/Ticket';
  import Crawler from '../components/Crawler';

  export default {
    data () {
      return {
        tabs: ['Ticket', 'Crawler', 'Utils'],
        active: null
      }
    },
    components: {
      Ticket, Crawler
    }
  }
</script>