<template>
  <div id="app">
    <v-app id="inspire" dark>
      <app-toolbar @toggleDrawer="toggleDrawer"></app-toolbar>
      <app-side-drawer :drawer='drawer'></app-side-drawer>
      <app-footer></app-footer>
      <v-content>
        <app-home></app-home>
      </v-content>
    </v-app>
  </div>
</template>

<script>

import AppToolbar from './components/AppToolbar'
import AppSideDrawer from './components/AppSideDrawer'
import AppFooter from './components/AppFooter'
import AppHome from './components/AppHome'

export default {
  name: 'App',
  components: {
    AppToolbar,
    AppSideDrawer,
    AppFooter,
    AppHome
  },
  data () {
    return {
      gitHubHook: "https://github.com/AaronWoods",
      siteTitle: "project-vuejs",
      drawer: true
    }
  },
  methods:{
    toggleDrawer : function(){
      this.drawer = !this.drawer
    }
  }

}
</script>
