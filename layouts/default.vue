<template>
<v-app id="keep">
    <v-app-bar app clipped-left color="amber">
        <v-app-bar-nav-icon @click="drawer = !drawer"></v-app-bar-nav-icon>
        <span class="title ml-3 mr-5">Calc&nbsp;<span class="font-weight-light">Material</span></span>
        <v-text-field solo-inverted flat hide-details label="Pesquisar"></v-text-field>

        <v-app-bar-nav-icon @click="drawerRight = !drawerRight"></v-app-bar-nav-icon>

    </v-app-bar>




    <v-content>
        <v-container>
            <nuxt />
        </v-container>  
    </v-content>

    <v-navigation-drawer v-model="drawerRight" app  clipped right color="grey lighten-4">
        <main-menu-right ref="MainMenuRight" />
    </v-navigation-drawer>
    
    <v-navigation-drawer v-model="drawer" app clipped color="grey lighten-4">
        <main-menu ref="MainMenu" />
    </v-navigation-drawer>

    <!--
    <v-footer :fixed="fixed" app>
        <span>&copy; {{ new Date().getFullYear() }}</span>
    </v-footer> -->
</v-app>
</template>

<script>
import MainMenu from "~/components/menu/MainMenu"
import MainMenuRight from "~/components/menu/MainMenuRight"
export default {

    components: {
        MainMenu,
        MainMenuRight

    },

    props: {
        source: String,
    },
    data: () => ({
        drawer: null,
        drawerRight: null,

    }),
}
</script>

<style>
#keep .v-navigation-drawer__border {
    display: none
}
</style>
