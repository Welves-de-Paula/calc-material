<template>
<v-app id="keep">
    <v-app-bar app clipped-left color="amber">
        <v-app-bar-nav-icon @click="drawer = !drawer"></v-app-bar-nav-icon>
        <span class="title ml-3 mr-5">Calc&nbsp;<span class="font-weight-light">Material</span></span>
        <v-text-field solo-inverted flat hide-details label="Pesquisar"></v-text-field>

        <v-spacer></v-spacer>
    </v-app-bar>

    <v-navigation-drawer v-model="drawer" app clipped color="grey lighten-4">
        <main-menu ref="MainMenu" />
    </v-navigation-drawer>

    <v-content>
        <v-container>
            <nuxt />
        </v-container>
    </v-content>

    <v-footer :fixed="fixed" app>
        <span>&copy; {{ new Date().getFullYear() }}</span>
    </v-footer>
</v-app>
</template>

<script>
import MainMenu from "~/components/menu/MainMenu"
export default {

    components: {
        MainMenu

    },

    props: {
        source: String,
    },
    data: () => ({
        drawer: null,

    }),
}
</script>

<style>
#keep .v-navigation-drawer__border {
    display: none
}
</style>
