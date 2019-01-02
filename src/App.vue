<template>
  <div id="app">
    <v-app id="inspire" dark>
      <app-toolbar @toggleDrawer="toggleDrawer"></app-toolbar>
      <app-side-drawer :drawer='drawer'></app-side-drawer>
      <app-footer></app-footer>
      <v-content>
        <router-view/>
      </v-content>
    </v-app>
  </div>
</template>

<script>

import AppToolbar from './components/AppToolbar'
import AppSideDrawer from './components/AppSideDrawer'
import AppFooter from './components/AppFooter'

export default {
  name: 'App',
  components: {
    AppToolbar,
    AppSideDrawer,
    AppFooter,
  },
  data () {
    return {
      gitHubHook: "https://github.com/AaronWoods",
      siteTitle: "project-vuejs",
      drawer: false
    }
  },
  methods:{
    toggleDrawer : function(){
      this.drawer = !this.drawer
    }
  }

}
</script>
