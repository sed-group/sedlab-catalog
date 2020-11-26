# Frontend setup

Install node and npm: <https://nodejs.org/en/download/>

Install vue-cli: <https://cli.vuejs.org/guide/installation.html>

``` bash
npm install -g @vue/cli
```

Install vuetify: <https://vuetifyjs.com/en/getting-started/installation/>

Create a new Vue project:

``` bash
vue create .
```

Choose Default settings: ([Vue 2] babel, eslint)

Add the Vuetify Vue CLI package:

``` bash
vue add vuetify
```

Choose default settings.

Start the development server:

``` bash
npm run serve
```

Visit <http://localhost:8080/>

Edit the files in ```src```.

Deploy in Netlify: <https://app.netlify.com/teams/inigoalonso/overview>

New site from Git > GitHub > sed-group

Build command:

```bash
npm run build
```

Directory: `dist`

Site now live and doing CI at <https://sedlab-catalog.netlify.app>

Add `db.json` to m,ock up API with <https://my-json-server.typicode.com/>

Add Axios for API fetching: <https://vuejs.org/v2/cookbook/using-axios-to-consume-apis.html>

```bash
npm install axios
```
