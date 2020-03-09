<template>
  <v-app>
    <v-app-bar
      app
    >
      <v-toolbar-title>Trello Clone</v-toolbar-title>
      <v-spacer></v-spacer>

      <v-btn flat  :to="{ name: 'Register'}">
         Register 
      </v-btn>

      <v-btn flat :to="{name: 'Login'}">
        Login
      </v-btn>
    </v-app-bar>

    <v-content>
    <router-view />

    </v-content>
  </v-app>
</template>

<script>

export default {
  name: 'App',
  data: () => ({
    //
  }),
};
</script>
