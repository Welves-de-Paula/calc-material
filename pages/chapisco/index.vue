<template>
<v-app>
    <v-row>
        <v-col>
            <span class="title">Calculo para Chapisco:</span>
            <v-row>

            </v-row>
            <v-row>

            </v-row>
            mm -> milímetros

            <v-row>
                <v-col cols="3" offset="3">
                    <v-text-field label=" Proporção Cimento" placeholder="Placeholder" outlined></v-text-field>
                </v-col>

                <v-col cols="3">
                    <v-text-field label=" Proporção Areia" placeholder="Placeholder" outlined></v-text-field>

                </v-col>

            </v-row>
            <v-row>
                <v-col cols="3" offset="3">
                    <v-text-field label=" Espessura do Chapisco" placeholder="Placeholder" outlined></v-text-field>

                </v-col>
                <v-col cols="3">
                    <v-text-field label="Área do Chapisco" placeholder="Placeholder" outlined></v-text-field>
                </v-col>

            </v-row>
            <v-row>
                <v-col cols="3" offset="3">
                    <v-text-field :label="'  Quantidade de cimento saco de 50 kg'" v-model="joint_width"></v-text-field>
                </v-col>
                <v-col cols="3" offset="0">
                    <v-text-field :label="'Quantidade de areia m3'" v-model="gasket_thickness"></v-text-field>
                </v-col>
            </v-row>
        </v-col>
        <v-col cols="4">
            <chapisco-table />

        </v-col>

    </v-row>

</v-app>
</template>

<script>
import chapiscoTable from "~/components/tables/chapiscoTable"
export default {
    components: {
        chapiscoTable
    },
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
