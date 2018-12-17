<template>
  <div id="app">
    <v-app id="inspire" dark>
      <v-navigation-drawer
        clipped
        fixed
        v-model="drawer"
        app
      >
        <v-list dense>
          <v-list-tile @click="doThis">
            <v-list-tile-action>
              <v-icon>dashboard</v-icon>
            </v-list-tile-action>
            <v-list-tile-content>
              <v-list-tile-title>Dashboard</v-list-tile-title>
            </v-list-tile-content>
          </v-list-tile>
          <v-list-tile @click="doThat">
            <v-list-tile-action>
              <v-icon>settings</v-icon>
            </v-list-tile-action>
            <v-list-tile-content>
              <v-list-tile-title>Settings</v-list-tile-title>
            </v-list-tile-content>
          </v-list-tile>
        </v-list>
      </v-navigation-drawer>
      <v-toolbar app fixed clipped-left>
        <v-toolbar-side-icon @click.stop="drawer = !drawer"></v-toolbar-side-icon>
        <v-toolbar-title>{{siteTitle}}</v-toolbar-title>
        <v-spacer></v-spacer>
      <v-btn
        flat
        :href="gitHubHook"
        target="_blank"
      >
        <span class="mr-2">Github</span>
      </v-btn>
      </v-toolbar>
      <v-content>
        
      </v-content>
      <v-footer app fixed>
        <span>&copy; 2017</span>
      </v-footer>
    </v-app>
  </div>
</template>

<script>

import Toolbar from './components/Toolbar'
export default {
  name: 'App',
  components: {
    Toolbar
  },
  data () {
    return {
      drawer: false,
      gitHubHook: "https://github.com/AaronWoods",
      siteTitle: "project-vuejs"
    }
  },
  methods:{
    doThis : function() {
      console.log("this");
    },
    doThat : function(){
      console.log("that");
    }
  }
}
</script>
