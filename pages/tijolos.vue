<template>
  <v-app>
    <link href="https://fonts.googleapis.com/icon?family=Material+Icons" rel="stylesheet" />
    <v-row>

    <v-row>
      <v-col cols="3" offset="1">
        <span class="title">Calculo para Tijolos</span>
      </v-col>
      <v-col cols="10" offset="4">
        <v-chip-group v-model="brick_area" mandatory>
          <v-chip filter outlined :value="0.04">Tijolo 0,20m X 0,20m</v-chip>
          <v-chip filter outlined :value="0.06">Tijolo 0,20m X 0,30m</v-chip>
          <v-chip filter outlined :value="0.08">Tijolo 0,20m X 0,40m</v-chip>
        </v-chip-group>
      </v-col>
    </v-row>
    </v-row>
    <template v-for="(row, index) in calcs">
      <v-row :key="index">
        <v-col cols="2" offset="4">
          <v-text-field :label="'Altura'" v-model="row.height"></v-text-field>
        </v-col>
        <v-col cols="2">
          <v-text-field :label="'Comprimento'" v-model="row.width"></v-text-field>
        </v-col>
        <v-col cols="2">
          <v-text-field :label="'Tijolos'" :disabled="true" :value="calc(row)"></v-text-field>
        </v-col>
        <v-col cols="2">
          <v-btn class="ma-2" outlined color="red" @click="removeRow(index)" v-if="hasMoreThanOneRow" >
            <span class="material-icons">delete_forever</span>
          </v-btn>
        </v-col>
      </v-row>
    </template>
    <v-row>
      <v-col cols="2" offset="5">
        <v-btn color="light-green accent-3" @click="addRow()">Nova Linha +</v-btn>
      </v-col>
      <v-col offset cols>
        <span class="title">Total: {{ total }}</span>
      </v-col>
    </v-row>
  </v-app>
</template>

<script>
export default {
  data: () => {
    return {
      brick_area: 0,
      calcs: [
        {
          height: 0,
          width: 0
        }
      ]
    };
  },

  computed: {
    total() {
      let total = 0;
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
        height: null,
        width: null
      });
    },

    removeRow(index) {
      this.calcs.splice(index, 1);
    },

    calc(row) {
      let result = (row.width * row.height) / this.brick_area;
      return Math.ceil(result);
    }
  }
};
</script>


