<template>
  <v-container>
    <v-row>
      <v-col cols="12">
        <v-row>
          <v-card
            v-for="(app, i) in catalog"
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
          <!-- <a
            :href="app.href"
            class="subheading mx-3"
            target="_blank"
          >
            {{ app.name }}
          </a> -->
        </v-row>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
  export default {
    name: 'Main',

    data: () => ({
      catalog: [
        {
          name: 'EF-M',
          href: 'https://github.com/sed-group/sedlab-efm',
          description: 'Lorem ipsum',
          contact: 'tbd',
          href_access: '',
          href_docs: '',
          href_source: 'https://github.com/sed-group/sedlab-efm',
        },
        {
          name: 'Morpheus',
          href: 'https://github.com/sed-group/morpheus',
          description: 'Lorem ipsum',
          contact: 'tbd',
          href_access: '',
          href_docs: '',
          href_source: 'https://github.com/sed-group/morpheus',
        },
        {
          name: 'Value',
          href: 'https://github.com/sed-group/sedlab-value',
          description: 'Lorem ipsum',
          contact: 'tbd',
          href_access: '',
          href_docs: '',
          href_source: 'https://github.com/sed-group/sedlab-value',
        },
        {
          name: 'Test',
          href: '',
          description: 'Lorem ipsum',
          contact: 'tbd',
          href_access: '',
          href_docs: '',
          href_source: '',
        },
        {
          name: 'Test',
          href: '',
          description: 'Lorem ipsum',
          contact: 'tbd',
          href_access: '',
          href_docs: '',
          href_source: '',
        },
        {
          name: 'Test',
          href: '',
          description: 'Lorem ipsum',
          contact: 'tbd',
          href_access: '',
          href_docs: '',
          href_source: '',
        },
        {
          name: 'Test',
          href: '',
          description: 'Lorem ipsum',
          contact: 'tbd',
          href_access: '',
          href_docs: '',
          href_source: '',
        },
        {
          name: 'Test',
          href: '',
          description: 'Lorem ipsum',
          contact: 'tbd',
          href_access: '',
          href_docs: '',
          href_source: '',
        },
      ],
    }),
  }
</script>
