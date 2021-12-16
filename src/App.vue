<template>
  <v-app>
    <!--Navbar -->
    <v-app-bar app color="primary" dark>
      <v-toolbar-title>Jacqueline Taylor & Friends</v-toolbar-title>
      <v-spacer></v-spacer>
      <v-btn
             v-for="link in links"
             :key="`${link.label}-header-link`"
             text
             rounded
             :to="link.url"> {{ link.label }}</v-btn>
     <!-- <v-btn text rounded to="/login">Login</v-btn> -->

    </v-app-bar>


    <v-content>
      <router-view></router-view>
    </v-content>

    <!-- Footer -->
    <v-footer color="primary" padless>
      <v-layout justify-center-wrap>
        <v-btn
          v-for="link in links"
          :key="`${link.label}-footer-link`"
          color="white"
          text
          class="my-2"
          :to="link.url"

        >{{ link.label }}</v-btn>
        <v-flex primary py-4 text-center white--text xs12>
          {{ new Date().getFullYear() }} - <strong> Bujisoft Dashboard</strong>
        </v-flex>
      </v-layout>
    </v-footer>

  </v-app>
</template>

<script>


export default {
  name: 'App',
  data () {
  return {

    links: [
      {
        label: 'Home',
        url: '/'
      },
      {
        label: 'Login',
        url: '/login'
      },
      {
        label: 'Dashboard',
        url: '/dashboard'
      }
    ]

  }
  }
  }
</script>
