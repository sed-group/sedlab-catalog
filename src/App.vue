<template>
  <v-app>
    <v-app-bar
      app
      dark
      color="#001436"
    >
      <v-toolbar-title class="headline text-uppercase">
        <span>SED</span>
        <span class="font-weight-light">Lab Catalog</span>
      </v-toolbar-title>

      <v-spacer></v-spacer>

      <v-btn
        href="https://sedlab-catalog.netlify.app/"
        target="_blank"
        text
      >
        <span class="mr-2">SEDLab</span>
        <v-icon>mdi-open-in-new</v-icon>
      </v-btn>
      <v-btn
        @click="overlay = !overlay"
        text
      >
        <span class="mr-2">Sign In</span>
        <v-icon>mdi-account</v-icon>
      </v-btn>
    </v-app-bar>

    <v-main>
      <video-bg :sources="['Lines-min.mp4']" img="Lines-min.png">
        <Main/>
      </video-bg>
    </v-main>
    <v-overlay :value="overlay">
      <v-card
        class="ma-2 pa-4"
        width="344"
        light
      >
        <v-form>
          <v-container>
            <v-row>
              <h1>Work In Progress</h1>
            </v-row>
            <v-row>
              <v-text-field
                v-model="email"
                label="E-mail"
                required
              ></v-text-field>
            </v-row>
            <v-row>
              <v-text-field
                v-model="password"
                label="password"
                required
              ></v-text-field>
            </v-row>
          </v-container>
        </v-form>
        <v-btn
          color="error"
          @click="overlay = false"
        >
          Close
        </v-btn>
      </v-card>
    </v-overlay>
  </v-app>
</template>

<script>
import Main from './components/Main';
import VideoBg from 'vue-videobg'

export default {
  name: 'App',

  components: {
    Main,
    VideoBg,
  },

  data: () => ({
    //
    overlay: false,
    email: null,
    password: null,
  }),
};
</script>
