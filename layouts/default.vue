<template>
  <v-app toolbar footer>
    <v-toolbar>
      <v-toolbar-title>Workit</v-toolbar-title>
      <v-spacer></v-spacer>
      <v-toolbar-side-icon class="hidden-md-and-up"></v-toolbar-side-icon>
      <v-toolbar-items class="hidden-sm-and-down">
          <v-btn to="/" flat>Ticket</v-btn>
          <v-btn to="/crawler" flat>Crawler</v-btn>
      </v-toolbar-items>
    </v-toolbar>
    <v-container fluid>
      <nuxt/>
    </v-container>
  </v-app>
</template>

<script>
  export default {
    data() {
      return {
        tabs: ['Ticket', 'Crawler', 'Utils'],
        active: null
      }
    }
  }
</script>