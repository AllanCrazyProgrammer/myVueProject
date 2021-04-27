<template>
  <div>
    <b-col>
      <h1>Cuentas</h1>
      <h2>{{ this.misDatos }}</h2>
    </b-col>
  </div>
</template>

<script>
import Datos from "./datos.vue";

export default {
  name: "Cuentas",
  props: ["misDatos","hello"],

  components: {
    Datos,
  },

  updated(){
   console.log(this.misDatos);

  },

  methods: {
    getCuentas(updateCuentas) {
      this.calculos = updateCuentas;
    },
  },
};
</script>

<style>
</style>