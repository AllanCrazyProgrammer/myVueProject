<template>
  <div>
    <b-col cols="1">
      <b-button v-on:click="getArray">Calcular</b-button>
    </b-col>

    <b-col cols="11">
      <Cuentas v-model="misDatos"/>
    </b-col>
  </div>
</template>

<script>
import Datos from "./datos.vue";
import Cuentas from "./Cuentas.vue";


export default {
  name: "Calcular",
  props: ["datos"],

  components: {
    Datos,Cuentas

  },

  data: () =>({
    misDatos: misDatos,
  }),


  methods: {
    getArray() {
      let misDatos = this.datos;
      misDatos = misDatos.split(`\n`).filter((x) => x);

      console.log(misDatos);
      return misDatos;
    },
  },
};
</script>

<style>
</style>