# vuetify-number

If you use Vuejs with Vuetify 2.x and you need a component to works with numbers (integer, decimal and percent), maybe this can help you.

input:
Numbers (integer, decimal and percent)

## Links
<p><a href="https://k6kzp.csb.app/">See DEMO here</a></p>
<p><a href="https://github.com/juareznasato/vuetify-simple-date" target="_blank">GitHub</a></p>
<p><a href="https://www.npmjs.com/package/vuetify-simple-date" target="_blank">npm</a></p>

## Install:
```
$ npm install vuetify-number --save

Register component:

1- Create a src/plugins/vuetify-number.js file with:
import Vue from "vue";
import VuetifyNumber from "vuetify-number";
Vue.use(VuetifyNumber);
export default VuetifyNumber;

2- Add to src/mains.js file:
import "./plugins/vuetify-number.js";

Parent component:
<template>
  <div>
    <vuetify-number
      v-model="value"
      v-bind:label="label"
      v-bind:disabled="disabled"
      v-bind:outlined="outlined"
      v-bind:options="options"
    />
    Parent v-model: {{ value }}
  </div>
</template>
<script>
export default {
  data: () => ({
    value: "123456789",
    label: "Value",
    readonly: false,
    disabled: false,
    outlined: true,
    clearable: true,
    options: {
      locale: "pt-BR",
      prefix: "R$",
      suffix: "",
      length: 9,
      precision: 2
    }
  })
};
</script>

