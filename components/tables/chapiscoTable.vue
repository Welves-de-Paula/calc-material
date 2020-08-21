<template>
<v-card class="mx-auto" max-width="500" tile>

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

    <v-list-item-group v-model="settings" multiple>
        <v-list-item>
            <template v-slot:default="{ active }">
                <v-list-item-action>
                    <v-checkbox :input-value="active" color="primary"></v-checkbox>
                </v-list-item-action>
                <v-list-item-content>
                    <v-list-item-title>Teto</v-list-item-title>
                </v-list-item-content>
            </template>
        </v-list-item>

        <v-list-item>
            <template v-slot:default="{ active }">
                <v-list-item-action>
                    <v-checkbox :input-value="active" color="primary"></v-checkbox>
                </v-list-item-action>

                <v-list-item-content>
                    <v-list-item-title>Superfície de concreto</v-list-item-title>
                </v-list-item-content>
            </template>
        </v-list-item>

        <v-list-item>
            <template v-slot:default="{ active }">
                <v-list-item-action>
                    <v-checkbox :input-value="active" color="primary"></v-checkbox>
                </v-list-item-action>

                <v-list-item-content>
                    <v-list-item-title>Parede</v-list-item-title>
                </v-list-item-content>
            </template>
        </v-list-item>
    </v-list-item-group>

    <v-list-item>
        <v-list-item-content>
            <v-list-item-title>Espesura</v-list-item-title>
        </v-list-item-content>
    <v-chip-group>
        <v-chip label  filter >Chapisco Grosso </v-chip>
        <v-chip label filter >Chapisco Fino</v-chip>
        <v-chip label filter > Personalizado</v-chip>
    </v-chip-group>
    </v-list-item>

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
