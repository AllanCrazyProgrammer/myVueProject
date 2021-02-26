<template>
  <div>
    <b-button v-on:click="getArray">Calcular</b-button>
  </div>
</template>

<script>
import Datos from "./datos.vue";

export default {
  name: "Cuentas",
  props: ["datos"],

  components: {
    Datos,
  },
  methods: {
    getArray() {
      let misDatos = this.datos;
      misDatos = misDatos.split(`\n`).filter((x) => x);

      console.log(misDatos);
      this.$emit("getArray");
      return misDatos;
    },
  },
};
</script>

<style>
</style>