<template>
  <v-toolbar app fixed clipped-left>
      <v-toolbar-side-icon @click.stop="toggleDrawer"></v-toolbar-side-icon>
      <router-link id="toolBarHomeButton" to="/">
        <v-toolbar-title >{{siteTitle}}</v-toolbar-title>
      </router-link>
      <v-spacer></v-spacer>
    <v-btn
      flat
      :href="gitHubHook"
      target="_blank"
    >
      <span class="mr-2">{{link1}}</span>
    </v-btn>
    </v-toolbar>
</template>

<script>
    export default {
      name: 'Toolbar',
      data () {
          return {
              gitHubHook: "https://github.com/AaronWoods",
              siteTitle: "project-vuejs",
              link1: "Github"
          }
      },
      methods:{
        toggleDrawer : function(){
          this.$emit('toggleDrawer')
        }
      }
  }
</script>

<style scoped>
#toolBarHomeButton {
  color: inherit;
  text-decoration: inherit;
}
</style>