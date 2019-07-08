<template>
  <div class="infoEscritor">
    <button
      class="btn btn-outline-dark"
      type="button"
      data-toggle="collapse"
      v-bind:data-target="'#'+'collapse'+escritor.id"
      aria-expanded="false"
      aria-controls="collapseExample"
    >{{escritor.nombre}}</button>
  </div>
</template>

<script>
export default {
  name: "Escritor",
  props: ["escritor"]
};
</script>

<style scoped>
    .infoEscritor {
        display: inline-block;
    }
</style>


