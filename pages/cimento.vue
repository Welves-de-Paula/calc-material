<template>
  <v-app>
      Calculo avançado
    <v-row>
      <v-list>
        <v-row>
        <v-col cols="10">
          <v-btn  @click="$router.push('/calc/advanced_calculus0')" text small><v-icon left>mdi-pencil</v-icon>Materiais para vigas</v-btn>
          <v-btn @click="$router.push('/calc/advanced_calculus1')" text small><v-icon left>mdi-pencil</v-icon>Materiais para piso de concreto</v-btn>
          <v-btn @click="$router.push('/calc/advanced_calculus2')" text small><v-icon left>mdi-pencil</v-icon>Materiais para laje de concreto</v-btn>
        </v-col>
        <v-col cols="12" offset="">

          <v-btn @click="$router.push('/calc/advanced_calculus3')" text small><v-icon left>mdi-pencil</v-icon>Quantidade de Materiais para Emboço</v-btn>
          <v-btn @click="$router.push('/calc/advanced_calculus4')" text small><v-icon left>mdi-pencil</v-icon>Quantidade de Materiais para chapisco</v-btn>
          <v-btn @click="$router.push('/calc/advanced_calculus5')" text small><v-icon left>mdi-pencil</v-icon>Materiais para Asentamento de tijolo furado</v-btn>
        </v-col>
        </v-row>

        <v-col cols="12">
          <v-btn @click="$router.push('/calc/advanced_calculus6')" text small><v-icon left>mdi-pencil</v-icon>Materiais para contrapiso de cimento e areia</v-btn>
          <v-btn @click="$router.push('/calc/advanced_calculus7')" text small><v-icon left>mdi-pencil</v-icon>Qantidade de Materiais para pilar embutido em parede de tijolo Furado</v-btn>
          <v-btn @click="$router.push('/calc/advanced_calculus8')" text small><v-icon left>mdi-pencil</v-icon>Materiais para pilar isolado ou embutido em paredes de bloco de concreto ou tijolo maciço</v-btn>
        </v-col>
      </v-list>
    </v-row>
  </v-app>
</template>

<script>
export default {};
</script>

<style>
</style>
