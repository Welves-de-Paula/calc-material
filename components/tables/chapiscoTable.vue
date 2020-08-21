<template>
<v-card class="mx-auto" max-width="400" tile>

    <v-list-item>
        <v-list-item-content>
            <v-list-item-title>Painel de configurçao rapida <v-icon class="ml-2" color="red">mdi-alert</v-icon>
            </v-list-item-title>
        </v-list-item-content>
    </v-list-item>

    <v-list-item>
        <v-list-item-content>
            <v-list-item-title>Finalidade</v-list-item-title>
        </v-list-item-content>

    </v-list-item>

    <v-list-item>
        <v-list-item-content>
            <v-list-item-title>Teto</v-list-item-title>
        </v-list-item-content>

    </v-list-item>

    <v-list-item>
        <v-list-item-content>
            <v-list-item-title>Superfície de concreto</v-list-item-title>
        </v-list-item-content>

    </v-list-item>
    <v-list-item>
        <v-list-item-content>
            <v-list-item-title>Parede</v-list-item-title>
        </v-list-item-content>
    </v-list-item>

    <span>Espesura</span>
    <v-chip-group>
        <v-chip filter class="ma-2">Chapisco Grosso 5</v-chip>
        <v-chip filter class="ma-2">Chapisco Fino 3</v-chip>
        <v-chip filter class="ma-2"> Personalizado</v-chip>
    </v-chip-group>

    <v-list-item>
        <v-list-item-content>
            <v-list-item-title>Area</v-list-item-title>
            <v-chip-group>

                <v-chip filter class="ma-2"> Pré calculada </v-chip>
                <v-chip filter class="ma-2"> Personalizado</v-chip>

            </v-chip-group>
        </v-list-item-content>

    </v-list-item>

</v-card>
</template>
