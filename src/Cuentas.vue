<template>
  <div>
    <b-col>
      <h1>Cuentas</h1>
      <h2>{{ this.datos }}</h2>
    </b-col>
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
};
</script>

<style>
</style>