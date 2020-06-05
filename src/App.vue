<template>
  <v-app id="inspire">
    <v-card-title>
      <v-toolbar dark class="elevation-2" color="cyan">
        <v-toolbar-title>vuetify-number</v-toolbar-title>
      </v-toolbar>
    </v-card-title>
    <v-card-text>
      <v-container>
        <v-row>
          <v-col cols="4" sm="4" md="4">
            <VuetifyNumber
              v-model="value"
              v-bind:label="label"
              v-bind:readonly="readonly"
              v-bind:disabled="disabled"
              v-bind:outlined="outlined"
              v-bind:clearable="clearable"
              v-bind:options="options"
            />
            Parent v-model: {{ value }}
            <br>
            Parent v-model null: {{ value === null ? "nulo" : "nao nulo" }}
            <br>
            Parent v-model "": {{ value === "" ? "vazio" : "nao vazio" }}
          </v-col>
        </v-row>
      </v-container>
    </v-card-text>
  </v-app>
</template>

<script>
import VuetifyNumber from "./components/VuetifyNumber.vue";

export default {
  name: "app",
  components: {
    VuetifyNumber
  },
  data: () => ({
    value: "1.23", // 1.23 or "1.23" or "" or null
    label: "Valor",
    readonly: false,
    disabled: false,
    outlined: true,
    clearable: true,
    valueWhenIsEmpty: "", // "0" or "" or null
    options: {
      locale: "pt-BR",
      prefix: "R$",
      suffix: "",
      length: 9,
      precision: 2,
    }
  })
};
</script>
