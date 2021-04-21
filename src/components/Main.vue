<template>
  <v-container>
    <v-row>
      <v-col cols="12">
        <v-row>
          <v-card
            v-for="(app, i) in applications"
            :key="i"
            class="d-flex flex-column ma-2"
            width="344"
            color="rgb(255, 255, 255, 0.7)"
          >
            <v-card-title>{{ app.name }}</v-card-title>
            <v-card-subtitle><strong>Lead: </strong>{{ app.contact }}</v-card-subtitle>
            <v-card-text>
              <div class="text--primary">
                {{ app.description }}
              </div>
            </v-card-text>
            <v-spacer></v-spacer>
            <v-card-actions>
              <v-btn
                text
                color="black accent-4"
                :href="app.href_source"
                target="_blank"
              >
                Source
              </v-btn>
              <v-btn
                text
                color="black accent-4"
                :href="app.href_docs"
                target="_blank"
              >
                Docs
              </v-btn>
              <v-btn
                text
                color="primary accent-4"
                :href="app.href_access"
                target="_blank"
              >
                Access
              </v-btn>
            </v-card-actions>
          </v-card>
          <v-alert
            dense
            outlined
            type="error"
            v-if="errorMessage!=null"
          >
            Error message: {{errorMessage}}
          </v-alert>
        </v-row>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
  import axios from 'axios';

  export default {
    name: 'Main',

    data: () => ({
      applications: null,
      errorMessage: null,
    }),
    created() {
      // GET request using axios with set headers
      const headers = { "Content-Type": "application/json" };
      //axios.get("https://test-app-afnkneebca-ew.a.run.app/applications", { headers })
      axios.get("https://my-json-server.typicode.com/sed-group/sedlab-catalog/applications", { headers })
        .then(response => this.applications = response.data)
        .catch(error => {
          this.errorMessage = error.message;
          console.error("There was an error!", error);
      });
    },
  }
</script>
