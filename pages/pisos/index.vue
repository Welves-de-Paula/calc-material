

<template  >
  <v-app>
    <link href="https://fonts.googleapis.com/icon?family=Material+Icons" rel="stylesheet" />
    <span class="title">Calculo para Pisos:</span>
    <template v-for="(row, index) in calcs">
      <v-row :key="index">
        <v-col cols="2" offset="2">
          <v-text-field :label="'Comprimento'" v-model="row.width"></v-text-field>
        </v-col>
        <v-col cols="2">
          <v-text-field :label="'Largura'" v-model="row.length"></v-text-field>
        </v-col>
        <v-col cols="3">
          <v-text-field :label="' Percentual de perca(%)'" v-model="row.loss"></v-text-field>
        </v-col>
        <v-col cols="2">
          <v-btn class="ma-2" outlined color="red" @click="removeRow(index)" v-if="hasMoreThanOneRow">
            <span class="material-icons">delete_forever</span>
          </v-btn>
        </v-col>
      </v-row>
    </template>


    <v-row>
      <v-col cols="1" offset="4">
        <v-btn color="light-green accent-3" @click="addRow()">Nova Linha +</v-btn>
      </v-col>
      <v-col offset="1" cols="4">
        <span class="title">Total: {{ total }}</span>
      </v-col>
    </v-row>
  </v-app>
</template>






<script>
export default {
  data: () => {
    return {
      calcs: [
        {
          loss: null,
          width: null,
          length: null
        }
      ]
    };
  },

  computed: {
    total() {
      let total = null;
      for (let index in this.calcs) {
        total = total + this.calc(this.calcs[index]);
      }
      return total;
    },

    hasMoreThanOneRow() {
      if (this.calcs.length > 1) {
        return true;
      } else {
        return false;
      }
    }
  },

  methods: {
    addRow() {
      this.calcs.push({
        loss: null,
        height: null,
        width: null
      });
    },

    removeRow(index) {
      this.calcs.splice(index, 1);
    },
    calc(row) {
      let result = row.width * row.length * (1 + row.loss / 100);

      return Math.ceil(result);
    }
  }
};
</script>


