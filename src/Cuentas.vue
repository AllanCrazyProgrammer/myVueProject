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
import Calcular from "./Calcular";


export default {
  name: "Cuentas",
  props: ["datos","misDatos"],

  components: {
    Datos,
    Calcular
  },

  methods: {
    getCuentas(){
      return
    }
  }
};


</script>

<style>
</style>