<template>
  <div>
    <b-row>
      <b-col cols="5">
        <textarea
          name="dinero"
          placeholder="Dinero"
          id=""
          cols="60"
          rows="60"
        ></textarea>
      </b-col>

      <b-col cols="1">
        <b-button>Calcular</b-button>
      </b-col>

      <b-col><h1>Cuentas</h1></b-col>
    </b-row>
  </div>
</template>

<script>
export default {
  name: "Datos",
  data() {
    return {};
  },
};
</script>

<style>
</style>