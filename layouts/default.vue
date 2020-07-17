<template>
  <v-app>
    <v-app-bar color="light-green accent-3" :clipped-left="clipped" fixed app>
      <v-toolbar-title v-text="title" />
      <v-spacer />
      <v-row>
        <v-tabs background-color="light-green accent-3">
          <v-tab @click="$router.push('/HOME')">HOME</v-tab>
          <v-tab @click="$router.push('/calc')">Calculo avançado</v-tab>
          <v-tab @click="$router.push('/cimento')">cimento</v-tab>
          <v-tab @click="$router.push('/pisos')">Pisos</v-tab>
          <v-tab @click="$router.push('/rejunte')">Rejuntes</v-tab>
          <v-tab @click="$router.push('/telhas')">telhas</v-tab>
          <v-tab @click="$router.push('/tijolos')">Tijolos</v-tab>
          <v-tab @click="$router.push('/Tintas')">Tintas</v-tab>
        </v-tabs>
      </v-row>
    </v-app-bar>

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
export default {
  data() {
    return {
      clipped: false,
      drawer: false,
      fixed: false,
      items: [
        {
          icon: "mdi-apps",
          title: "Welcome",
          to: "/"
        },
        {
          icon: "mdi-chart-bubble",
          title: "Inspire",
          to: "/inspire"
        }
      ],
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: "Calc"
    };
  }
};
</script>
