<template>
  <div class="mt-5">
    <b-row>
      <b-col cols="5">
        <textarea
          class="text-center"
          name="dinero"
          placeholder="Dinero"
          id=""
          cols="60"
          rows="60"
          v-model="datos"
        ></textarea>
      </b-col>

      <b-col cols="1">
        <b-button>Calcular</b-button>
      </b-col>

      <b-col cols="6">
        <Cuentas v-bind:datos="datos" />
      </b-col>
    </b-row>
  </div>
</template>


<script>
import Cuentas from "./Cuentas.vue";

export default {
  name: "Datos",
  components: {
    Cuentas,
  },
  data() {
    return {
      datos: "",
    };
  },
};
</script>

<style>
</style>