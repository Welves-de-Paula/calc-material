<template>
  <v-list-item>
            <v-list-item-content>
                <v-list-item-title @click="$router.push('/HOME')">HOME</v-list-item-title>
                <v-list-item-title @click="$router.push('/calc')">Calculo avançado</v-list-item-title>
                <v-list-item-title @click="$router.push('/cimento')">cimento</v-list-item-title>
                <v-list-item-title @click="$router.push('/pisos')">Pisos</v-list-item-title>
                <v-list-item-title @click="$router.push('/rejunte')">Rejuntes</v-list-item-title>
                <v-list-item-title @click="$router.push('/telhas')">telhas</v-list-item-title>
                <v-list-item-title @click="$router.push('/tijolos')"> Tijolos</v-list-item-title>
                <v-list-item-title @click="$router.push('/Tintas')">Tintas</v-list-item-title>
            </v-list-item-content>
        </v-list-item>
</template>

<script>
export default {

}
</script>

<style>

</style>
