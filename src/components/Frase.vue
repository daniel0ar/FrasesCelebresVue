<template>
  <div class="collapse" v-bind:id="'collapse'+id">
    <div class="card card-body">
        {{texto}}
    </div>
  </div>
</template>

<script>
export default {
  name: "Frase",
  components: {
  },
  props: ["id","texto"]
};
</script>

<style scoped>
</style>


