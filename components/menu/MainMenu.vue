<template>
<v-navigation-drawer v-model="drawer" :clipped="$vuetify.breakpoint.lgAndUp" app>
    <v-list dense>
        <template>
            <v-row align="center">
                <v-col cols="6">
                    <v-subheader>
                        tes
                    </v-subheader>
                </v-col>
                <v-col cols="6" class="text-center">
                    <a href="#!" class="body-2 black--text">EDIT</a>
                </v-col>
            </v-row>
            <v-list-group>
                <template v-slot:activator>
                    <v-list-item-content>
                        <v-list-item-title>
                            item.text
                        </v-list-item-title>
                    </v-list-item-content>
                </template>
                <v-list-item  link>
                    <v-list-item-action >
                        <v-icon>gr</v-icon>
                    </v-list-item-action>
                    <v-list-item-content>
                        <v-list-item-title>
                           g
                        </v-list-item-title>
                    </v-list-item-content>
                </v-list-item>
            </v-list-group>
            <v-list-item >
                <v-list-item-action>
                    <v-icon>gg</v-icon>
                </v-list-item-action>
                <v-list-item-content>
                    <v-list-item-title>
                        t
                    </v-list-item-title>
                </v-list-item-content>
            </v-list-item>
        </template>
    </v-list>
</v-navigation-drawer>

<!-- <v-list>
  <span></span>
    <v-list-item >

        <v-list-item-content>
            <v-list-item-title>Categorias</v-list-item-title>
        </v-list-item-content>
    </v-list-item>
    <v-list-item link @click.stop="$router.push('/cimento')">
        <v-list-item-icon>
            <v-icon>mdi-keg</v-icon>
        </v-list-item-icon>
        <v-list-item-content>
            <v-list-item-title>Cimento</v-list-item-title>
        </v-list-item-content>
    </v-list-item>

    <v-list-item link @click.stop="$router.push('/pisos')">
        <v-list-item-icon>
            <v-icon>mdi-floor-plan</v-icon>
        </v-list-item-icon>
        <v-list-item-content>
            <v-list-item-title>Pisos</v-list-item-title>
        </v-list-item-content>
    </v-list-item>

    <v-list-item link @click.stop="$router.push('/rejunte')">
        <v-list-item-icon>
            <v-icon>mdi-bag-personal-outline</v-icon>
        </v-list-item-icon>
        <v-list-item-content>
            <v-list-item-title>Rejunte</v-list-item-title>
        </v-list-item-content>
    </v-list-item>

    <v-list-item link @click.stop="$router.push('/telhas')">
        <v-list-item-icon>
            <v-icon>mdi-home-roof</v-icon>
        </v-list-item-icon>
        <v-list-item-content>
            <v-list-item-title>Telhas</v-list-item-title>
        </v-list-item-content>
    </v-list-item>

    <v-list-item link @click.stop="$router.push('/tijolos')">
        <v-list-item-icon>
            <v-icon>mdi-wall</v-icon>
        </v-list-item-icon>
        <v-list-item-content>
            <v-list-item-title>Tijolos</v-list-item-title>
        </v-list-item-content>
    </v-list-item>

    <v-list-item link @click.stop="$router.push('/tintas')">
        <v-list-item-icon>
            <v-icon>mdi-format-paint</v-icon>
        </v-list-item-icon>
        <v-list-item-content>
            <v-list-item-title>Tintas</v-list-item-title>
        </v-list-item-content>
    </v-list-item>

    <v-list-item link @click.stop="$router.push('/tintas')">
        <v-list-item-icon>
            <v-icon>mdi-alert</v-icon>
        </v-list-item-icon>
        <v-list-item-content>
            <v-list-item-title>Avançado</v-list-item-title>
        </v-list-item-content>
    </v-list-item>

</v-list> -->
</template>

<script>
export default {
    data: () => {
        return {
            drawer: false,
            height: null,
            width: null,
            length: null,
            cement_ratio: null,
            gravel_proportion: null,
            sand_ratio: null,
            amount_sand: 0,
            gravel: 0,
            cement_amount: 0,
            cement_result: null
        };
    },

}
</script>

<style>

</style>
