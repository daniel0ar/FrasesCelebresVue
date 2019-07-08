<template>
  <div id="tablaEscritores" class="container">
    <div class="escritor-info" v-bind:key="escritor.id" v-for="escritor in escritores">
      <Escritor v-bind:escritor="escritor"></Escritor>
      <div v-bind:key="frase.id_autor" v-for="frase in frases">
        <Frase v-bind:id="escritor.id" v-if="frase.id_autor==escritor.id" v-bind:texto="frase.texto" ></Frase>
      </div>
    </div>
  </div>
</template>

<script>
import Escritor from "./Escritor";
import Frase from "./Frase";

export default {
  name: "Escritores",
  components: {
    Escritor,
    Frase
  },
  props: ["escritores", "frases"]
};
</script>

<style scoped>
.escritor-info {
  display: inline-block;
}
</style>
