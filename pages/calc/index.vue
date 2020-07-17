<template>
  <v-app>
    <span class="title">Calculo avançado:</span>
    <span class="subtitle">Materiais para vigas</span>
    <v-row>
      <v-col cols="3">
        <v-text-field v-model="cement_ratio" label="Proporção de Cimento"></v-text-field>
        <v-text-field v-model="sand_ratio" label="Propoção de areia"></v-text-field>
        <v-text-field v-model="gravel_proportion" label="propoção de brita"></v-text-field>
        <v-text-field v-model="width" label="Largura da Viga"></v-text-field>
        <v-text-field v-model="height" label="alturagura da Viga"></v-text-field>
        <v-text-field v-model="length" label="Comptimento total da viga"></v-text-field>
      </v-col>

      <v-col>
        <span>
          Resultado:
          <v-row>
            <v-col>
              quantidade de areia
              <v-text-field
                background-color="success"
                dark
                v-model="amount_sand"
                label="Solo"
                solo
                readonly
              ></v-text-field>
            </v-col>

            <v-col>
              Quantidade de cimento
              <v-text-field
                background-color="success"
                dark
                v-model="cement_amount"
                label="Solo"
                solo
                readonly
              ></v-text-field>
            </v-col>

            <v-col>
              quantidade de brita
              <v-text-field
                background-color="success"
                dark
                v-model="gravel"
                label="Solo"
                solo
                readonly
              ></v-text-field>
            </v-col>

            <v-btn @click="setResult()" color="success" block>Calcular</v-btn>
          </v-row>
        </span>
      </v-col>
    </v-row>
  </v-app>
</template>


<script>
export default {
  data: () => {
    return {
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
  methods: {
    setResult() {
      var gravel = (this.length * this.width *this.height * 0.7) / 10000;
      var gravel = gravel.toFixed(2);

      var amount_sand =
        (gravel / this.gravel_proportion) * this.sand_ratio;

      var amount_sand = amount_sand.toFixed(2);

      var cement_amount = ((gravel / this.gravel_proportion) * 1400) / 50;

      var cement_amount =  cement_amount.toFixed(2);
    }
  }
};
</script>
