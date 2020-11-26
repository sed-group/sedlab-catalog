<template>
  <v-app>
    <v-app-bar
      app
      color="indigo"
      dark
    >
      <v-toolbar-title class="headline text-uppercase">
        <span>SED</span>
        <span class="font-weight-light">Lab</span>
      </v-toolbar-title>

      <v-spacer></v-spacer>

      <v-btn
        href="https://github.com/sed-group/sedlab-catalog"
        target="_blank"
        text
      >
        <span class="mr-2">GitHub</span>
        <v-icon>mdi-open-in-new</v-icon>
      </v-btn>
      <v-btn
        href=""
        text
      >
        <span class="mr-2">Sign In</span>
        <v-icon>mdi-account</v-icon>
      </v-btn>
    </v-app-bar>

    <v-main>
      <Main/>
    </v-main>
  </v-app>
</template>

<script>
import Main from './components/Main';

export default {
  name: 'App',

  components: {
    Main,
  },

  data: () => ({
    //
  }),
};
</script>
