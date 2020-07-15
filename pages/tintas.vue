<template  >
  <v-app>
    <span class="title">Calcular Tintas</span>
    <v-row>
      <v-col cols="4" offset="4">
        <span>1° Selecione o Número de demão:</span>
        <v-overflow-btn :items="numbers_of_coat" v-model="number_of_coat" label="Número de demão"></v-overflow-btn>
      </v-col>
    </v-row>
    <v-row>
      <v-col cols="3" offset="4">
        2° Redimento do produto:
        <v-text-field v-model="product_yield"></v-text-field>
      </v-col>
    </v-row>
    <v-row>
      <v-col cols="3" offset="4">
        <span>3° Área a ser pintada</span>
      </v-col>
    </v-row>

    <v-row>
      <v-col cols="2" offset="4">
        <v-text-field :label="'Altura'" v-model="length"></v-text-field>
      </v-col>
      <v-col cols="2">
        <v-text-field :label="'Comprimento'" v-model="width"></v-text-field>
      </v-col>
      <v-col cols="4" offset="4">
        <v-btn color="success" @click="this.setcalc">Calcular</v-btn>.
      </v-col>
    </v-row>
    <v-row>
      <v-col cols="4" offset="4">
        <span class="title">Quantidade de Tinta necessária (Litros)</span>
        <v-text-field background-color="success" dark v-model="total" label solo readonly></v-text-field>
      </v-col>
    </v-row>
  </v-app>
</template>

<script>
export default {
  data: () => {
    return {
      numbers_of_coat: ["1", "2", "3", "4"],
      number_of_coat: null,
      width: null,
      length: null,
      product_yield: null,
      total: 0,
      wall_area: 0
    };
  },

  methods: {
    setcalc() {
      this.total =
        (this.width * this.length * this.number_of_coat) / this.product_yield;
    }
  }
};
</script>
