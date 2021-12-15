<template>
  <v-app>
    <!--Navbar -->
    <v-app-bar app color="primary" dark>
      <v-toolbar-title>Jacqueline Taylor & Friends</v-toolbar-title>
      <v-spacer></v-spacer>
      <v-btn text rounded>Home</v-btn>
      <v-btn text rounded>Login</v-btn>

    </v-app-bar>

    <!-- end navbar -->


<!-- WRAP CONTENT TO REOMOVE OVERLAPPING -->

    <v-content>

      <h1>test</h1>
    <!-- LOGIN MODULE
    <v-card width="460px" class=" mx-auto mt-5">
      <v-card-title class="pb-0">
        <h1 class="display-1">Jacqueline Taylor & Friends</h1>
      </v-card-title>
      <v-card-text>
        <v-form>
          <v-text-field label ="Username" prepend-icon="mdi-account-circle"/>
          <v-text-field :type ="showPassword ? 'text' : 'password' "
                        label ="Password"
                        prepend-icon="mdi-lock"
                        :append-icon="showPassword ? 'mdi-eye' : 'mdi-eye-off'"
                        @click:append="showPassword = !showPassword"/>
        </v-form>
      </v-card-text>
      <v-divider></v-divider>
        <v-card-actions>
          <v-btn color="success">Register</v-btn>
          <v-spacer></v-spacer>
          <v-btn color="info">Login</v-btn>
        </v-card-actions>


    </v-card>

end login -->
    </v-content>

    <!-- Footer -->
    <v-footer color="primary" padless>
      <v-layout justify-center-wrap>
        <v-btn
          v-for="link in links"
          :key="link"
          color="white"
          text
          class="my-2">{{ link }}</v-btn>
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
    //showPassword: false,
    links: ['Home', 'Login']

  }
  }
  }
</script>
