<template>
<div>
    <v-icon color="red"> mdi-alert</v-icon>
    <v-row>
        <v-btn @click.stop="$router.push('/pilar-isolado')">pilar isolado</v-btn>

        <v-btn @click.stop="$router.push('/pilar-embutido')">Pilar embutido </v-btn>
    </v-row>
    <v-row>
        <v-btn @click.stop="$router.push('/contrapiso')">Contrapiso</v-btn>

        <v-btn @click.stop="$router.push('/emboço')">Emboço</v-btn>
        <v-btn @click.stop="$router.push('/chapisco')">Chapisco</v-btn>
    </v-row>
    <v-row>
        <v-btn @click.stop="$router.push('/vigas')"> vigas</v-btn>
        <v-btn @click.stop="$router.push('/laje')">Laje de concreto</v-btn>
    </v-row>

    <!-- <span>Materiais Para Assentamento de tijolo furado</span> -->

    <!-- <v-btn @click.stop="$router.push('/advanced')">Materiais para piso de concreto</v-btn> -->

    <!-- <span>Argamassa e Rejunte para Assentamento de cerâmica</span> -->

</div>
</template>

<script>
export default {


}
</script>

<style>

</style>
