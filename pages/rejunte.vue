<template>
  <v-app>

    <span class="title">Calculo para rejunte:</span>
    <v-row>
      <v-col offset="2">
        <v-chip-group v-model="grout" mandatory>
          <v-chip filter outlined :value="1.58">Epóxi</v-chip>
          <v-chip filter outlined :value="1.75">Flexivel</v-chip>
          <v-chip filter outlined :value="1.49">Fluido</v-chip>
          <v-chip filter outlined :value="1.32">Rejunte sobre rejunte</v-chip>

          <v-chip filter outlined :value="1.76">Fachadas</v-chip>
          <v-chip
            filter
            outlined
            :value="1.62"
          >Pedras Rústicas, Piscinas, Porcelanatos, Mármore e Granitos</v-chip>
        </v-chip-group>
      </v-col>
    </v-row>
    <v-row>
      <v-col cols="4" offset="3">
        <span class="title">Tamanho do Revestimento (Milímetros)</span>
      </v-col>
    </v-row>

    <v-row>
      <v-col cols="3" offset="3">
        <v-text-field :label="'Comprimento (Milímetros)'" v-model="width_mm"></v-text-field>
      </v-col>

      <v-col cols="3">
        <v-text-field :label="'Largura (Milímetros)'" v-model="length_mm"></v-text-field>
      </v-col>
    </v-row>

    <v-row>
      <v-col cols="3" offset="3">
        <v-text-field
          :label="'Largura da junta de assentamento (Milímetros):'"
          v-model="joint_width"
        ></v-text-field>
      </v-col>
      <v-col cols="3" offset="0">
        <v-text-field
          :label="'Espessura da junta de assentamento (Milímetros):'"
          v-model="gasket_thickness"
        ></v-text-field>
      </v-col>
    </v-row>
    <v-row>
      <v-col cols="6" offset="3">
        <span class="title">Área a ser rejuntada:</span>
      </v-col>
    </v-row>
    <v-row>
      <v-col cols="3" offset="3">
        <v-text-field :label="' Digite a largura (Em Metros):'" v-model="area_width"></v-text-field>
      </v-col>
      <v-col cols="3" offset="0">
        <v-text-field :label="' Digite o comprimento( em Metros):'" v-model="length_area"></v-text-field>
      </v-col>
    </v-row>
    <v-row>
      <v-col cols="4" offset="4">
        <v-btn @click="calc()" color="success" block>Calcular</v-btn>
      </v-col>
    </v-row>
    <v-row>
      <v-col cols="3" offset="3">
        Total de Kg/m²
        <v-text-field background-color="success" dark v-model="result" label solo readonly></v-text-field>
      </v-col>
      <v-col cols="3" offset>
        Total geral (Quilos de rejunte)
        <v-text-field background-color="success" dark v-model="grand_total" label solo readonly></v-text-field>
      </v-col>
    </v-row>

  </v-app>
</template>


<script>
export default {
  data: () => {
    return {
      joint_width: null,
      gasket_thickness: null,

      length_mm: null,
      length_area: null,
      area_width: null,
      grand_total: 0,
      area: null,

      width_mm: null,
      soma: 0,
      area: 0,
      total: 0,

      grout: null,
      result: 0
    };
  },

  methods: {
    calc() {
      this.soma = parseInt(this.length_mm) + parseInt(this.width_mm);
      this.total = this.gasket_thickness * this.joint_width * this.grout;
      this.area = this.length_mm * this.width_mm;
      this.result = (this.soma * this.total) / this.area;
      this.area = this.length_area * this.area_width;
      this.grand_total = this.result * this.area;
    }
  }
};
</script>



