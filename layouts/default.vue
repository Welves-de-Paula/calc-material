<template>
<v-app id="inspire">
    <v-navigation-drawer width="300" v-model="drawer"  app clipped color="transparent">
        <main-menu  ref="MainMenu" />
    </v-navigation-drawer>

    <v-app-bar :clipped-left="$vuetify.breakpoint.lgAndUp" app color="blue darken-3" dark>
        <v-app-bar-nav-icon @click.stop="drawer = !drawer"></v-app-bar-nav-icon>
        <v-toolbar-title style="width: 300px" class="ml-0 pl-4">
            <span class="hidden-sm-and-down">Calc Material</span>
        </v-toolbar-title>
        <v-text-field flat solo-inverted hide-details prepend-inner-icon="mdi-magnify" label="Search" class="hidden-sm-and-down"></v-text-field>
        <v-spacer></v-spacer>
        <v-btn icon>
            <v-icon>mdi-apps</v-icon>
        </v-btn>
        <v-btn icon>
            <v-icon>mdi-bell</v-icon>
        </v-btn>
        <v-btn icon large>
            <v-avatar size="32px" item>
                <v-img src="https://cdn.vuetifyjs.com/images/logos/logo.svg" alt="Vuetify"></v-img>
            </v-avatar>
        </v-btn>
    </v-app-bar>

    <v-content>
        <v-container>
            <nuxt />
        </v-container>
    </v-content>
    <dialog-print />

</v-app>
</template>

<script>
import MainMenu from "~/components/menu/MainMenu"
import DialogPrint from "~/components/tools/DialogPrint"

export default {
    props: {
        source: String,
    },

    components: {
        MainMenu,
        DialogPrint

    },

    data: () => ({
        dialog: false,
        drawer: null,

    }),
}
</script>
