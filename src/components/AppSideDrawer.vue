<template>
    <v-navigation-drawer
            clipped
            fixed
            v-model="drawer"
            app
        >
        <v-list dense>
            <v-list-tile :to="{path:'/about'}" @click="doThis">
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
</template>

<script>
export default {
    name: "SideDrawer",
    props: [
        'drawer'
    ],
    data() {
        return {
            
        }
    },
    methods:{
        doThis: function(){

        },
        doThat: function(){
            
        }
    }
}
</script>


