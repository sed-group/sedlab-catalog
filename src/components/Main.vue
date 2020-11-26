<template>
  <v-container>
    <v-row>
      <v-col cols="12">
        <v-row>
          <v-card
            v-for="(app, i) in applications"
            :key="i"
            class="ma-2"
            width="344"
          >
            <v-card-title>{{ app.name }}</v-card-title>
            <v-card-subtitle>Testing</v-card-subtitle>
            <v-card-text>
              <div class="text--primary">
                <strong>Description: </strong>{{ app.description }}
                <br />
                <strong>Contact: </strong>{{ app.contact }}
              </div>
            </v-card-text>
            <v-card-actions>
              <v-btn
                text
                color="indigo accent-4"
                :href="app.href_source"
                target="_blank"
              >
                Source
              </v-btn>
              <v-btn
                text
                color="indigo accent-4"
                :href="app.href_docs"
                target="_blank"
              >
                Docs
              </v-btn>
              <v-btn
                text
                color="success accent-4"
                :href="app.href_access"
                target="_blank"
              >
                Access
              </v-btn>
            </v-card-actions>
          </v-card>
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
    }),
    created() {
      // Simple GET request using axios
      axios.get("https://my-json-server.typicode.com/sed-group/sedlab-catalog/applications")
        .then(response => this.applications = response.data);
    },
  }
</script>
