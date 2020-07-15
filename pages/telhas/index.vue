<template>
  <v-app>

    <span class="title">Calculo paraTelhas</span>
    <v-row>
      <v-col offset="4">
        <v-chip-group v-model="roofArea" mandatory>
          <v-chip filter outlined :value="2.684">Telha Amianto 1,10m x 2,44m</v-chip>
          <v-chip filter outlined :value="1.22">Telha Amianto 0,50m x 2,44m</v-chip>
        </v-chip-group>
      </v-col>
    </v-row>
    <v-row>
      <v-col cols="3" offset="4">
        <span>Digite o comprimento (M)</span>
        <v-text-field v-model="width"></v-text-field>
      </v-col>
      <v-col cols="3" offset="4">
        Digite a largura (M)
        <v-text-field v-model="length"></v-text-field>
      </v-col>
    </v-row>

    <v-row>
      <v-col cols="4" offset="4">
        <v-btn @click="calc()" color="success" block>Calcular</v-btn>
      </v-col>
    </v-row>

    <template v-if="result !== null">
      <v-row>
        <v-col cols="2" offset="4">
          Total de telhas:
          <v-text-field background-color="success" dark v-model="result" label="Solo" solo readonly></v-text-field>
        </v-col>

        <v-col cols="2" offset="">
          total de parafusos:
         <v-text-field background-color="success" dark v-model="nail" label="Solo" solo readonly></v-text-field>
        </v-col>
      </v-row>
    </template>


  </v-app>
</template>

<script>
export default {
  data: () => {
    return {
      roofArea: null,
      width: 0,
      length: 0,
      nail: 0,
      result: null
    };
  },
  methods: {
    calc() {
      let result = (this.width * this.length) / this.roofArea;

      this.nail = Math.ceil(result * 3);

      this.result = Math.ceil(result);
    }
  }
};
</script>


