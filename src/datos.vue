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

      <b-col cols="7">
        <Calcular v-bind:datos="datos"/>
      </b-col>


    </b-row>
  </div>
</template>


<script>
import Calcular from "./Calcular";


export default {
  name: "Datos",
  components: {
    Calcular
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