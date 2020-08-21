<template>
<div>
    <v-expansion-panels v-model="panel" multiple>
        <v-expansion-panel>
            <v-expansion-panel-header>Cimento</v-expansion-panel-header>
            <v-expansion-panel-content>

                <v-list>
                    <v-list-item link @click.stop="$router.push('/chapisco')">
                        <v-list-item-icon>
                            <!-- <v-icon>mdi-keg</v-icon> -->
                        </v-list-item-icon>
                        <v-list-item-content>
                            <v-list-item-title>Chapisco</v-list-item-title>
                        </v-list-item-content>
                    </v-list-item>

                    <v-list-item link @click.stop="$router.push('/emboço')">
                        <v-list-item-icon>
                            <!-- <v-icon>mdi-floor-plan</v-icon> -->
                        </v-list-item-icon>
                        <v-list-item-content>
                            <v-list-item-title>Emboço</v-list-item-title>
                        </v-list-item-content>
                    </v-list-item>

                    <v-list-item link @click.stop="$router.push('/emboço')">
                        <v-list-item-icon>
                            <!-- <v-icon>mdi-floor-plan</v-icon> -->
                        </v-list-item-icon>
                        <v-list-item-content>
                            <v-list-item-title>Vigas</v-list-item-title>
                        </v-list-item-content>
                    </v-list-item>

                    <v-list-item link @click.stop="$router.push('/pilar-embutido')">
                        <v-list-item-icon>
                            <!-- <v-icon>mdi-bag-personal-outline</v-icon> -->
                        </v-list-item-icon>
                        <v-list-item-content>
                            <v-list-item-title>Pilar Embutido</v-list-item-title>
                        </v-list-item-content>
                    </v-list-item>

                    <v-list-item link @click.stop="$router.push('/pilar-isolado')">
                        <v-list-item-icon>
                            <!-- <v-icon>mdi-home-roof</v-icon> -->
                        </v-list-item-icon>
                        <v-list-item-content>
                            <v-list-item-title>Pilar Isolado</v-list-item-title>
                        </v-list-item-content>
                    </v-list-item>

                </v-list>

            </v-expansion-panel-content>
        </v-expansion-panel>

        <v-expansion-panel>
            <v-expansion-panel-header>Paredes</v-expansion-panel-header>
            <v-expansion-panel-content>

                <v-list>
                    <v-list-item link @click.stop="$router.push('/tintas')">
                        <v-list-item-icon>
                            <!-- <v-icon>mdi-keg</v-icon> -->
                        </v-list-item-icon>
                        <v-list-item-content>
                            <v-list-item-title>Tintas</v-list-item-title>
                        </v-list-item-content>
                    </v-list-item>

                    <v-list-item link @click.stop="$router.push('/tijolos')">
                        <v-list-item-icon>
                            <!-- <v-icon>mdi-floor-plan</v-icon> -->
                        </v-list-item-icon>
                        <v-list-item-content>
                            <v-list-item-title>Tijolos</v-list-item-title>
                        </v-list-item-content>
                    </v-list-item>
                </v-list>

            </v-expansion-panel-content>
        </v-expansion-panel>

        <v-expansion-panel>
            <v-expansion-panel-header>Acabamentos</v-expansion-panel-header>
            <v-expansion-panel-content>

                <v-list>
                    <v-list-item link @click.stop="$router.push('/tintas')">
                        <v-list-item-icon>
                            <!-- <v-icon>mdi-keg</v-icon> -->
                        </v-list-item-icon>
                        <v-list-item-content>
                            <v-list-item-title>Tintas</v-list-item-title>
                        </v-list-item-content>
                    </v-list-item>
                </v-list>

            </v-expansion-panel-content>
        </v-expansion-panel>

        <v-expansion-panel>
            <v-expansion-panel-header>Corberturas</v-expansion-panel-header>
            <v-expansion-panel-content>
                <v-list>
                    <v-list-item link @click.stop="$router.push('/telhas')">
                        <v-list-item-icon>
                            <!-- <v-icon>mdi-keg</v-icon> -->
                        </v-list-item-icon>
                        <v-list-item-content>
                            <v-list-item-title>Telhas</v-list-item-title>
                        </v-list-item-content>
                    </v-list-item>

                    <v-list-item link @click.stop="$router.push('/laje')">
                        <v-list-item-icon>
                            <!-- <v-icon>mdi-floor-plan</v-icon> -->
                        </v-list-item-icon>
                        <v-list-item-content>
                            <v-list-item-title>Laje</v-list-item-title>
                        </v-list-item-content>
                    </v-list-item>
                </v-list>

            </v-expansion-panel-content>
        </v-expansion-panel>

        <v-expansion-panel>
            <v-expansion-panel-header>Pisos</v-expansion-panel-header>
            <v-expansion-panel-content>
                <v-list>
                    <v-list-item link @click.stop="$router.push('/rejunte')">
                        <v-list-item-icon>
                            <!-- <v-icon>mdi-keg</v-icon> -->
                        </v-list-item-icon>
                        <v-list-item-content>
                            <v-list-item-title>Rejunte</v-list-item-title>
                        </v-list-item-content>
                    </v-list-item>

                    <v-list-item link @click.stop="$router.push('/contrapiso')">
                        <v-list-item-icon>
                            <!-- <v-icon>mdi-floor-plan</v-icon> -->
                        </v-list-item-icon>
                        <v-list-item-content>
                            <v-list-item-title>Contrapiso</v-list-item-title>
                        </v-list-item-content>
                    </v-list-item>
                    <v-list-item link @click.stop="$router.push('/contrapiso')">
                        <v-list-item-icon>
                            <!-- <v-icon>mdi-floor-plan</v-icon> -->
                        </v-list-item-icon>
                        <v-list-item-content>
                            <v-list-item-title>Piso de concreto</v-list-item-title>
                        </v-list-item-content>
                    </v-list-item>

                </v-list>

            </v-expansion-panel-content>
        </v-expansion-panel>
    </v-expansion-panels>
</div>
</template>

<script>
    export default {
        data: () => ({
            panel: [0, 1],
            disabled: false,
        }),
    }
</script>

<!--<template>
<v-list>
    <v-list-item>
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

</v-list>
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
