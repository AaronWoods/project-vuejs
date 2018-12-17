<template>
    <v-toolbar dark app>
      <v-toolbar-side-icon></v-toolbar-side-icon>
      <v-toolbar-title class="headline text-uppercase">
        <span>Project</span>
        <span class="font-weight-light">-vuejs</span>
      </v-toolbar-title>
      <v-spacer></v-spacer>
      <v-btn
        flat
        :href="gitHubHook"
        target="_blank"
      >
        <span class="mr-2">Github</span>
      </v-btn>
    </v-toolbar>
</template>

<script>
    export default {
        name: 'Toolbar',
    data () {
        return {
            gitHubHook: "https://github.com/AaronWoodsss"
        }
    }
  }
</script>