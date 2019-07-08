<template>
  <div id="app">
    <h1>Frases Celebres</h1>
    <Escritores v-bind:escritores="escritores" v-bind:frases="frases"/>
  </div>
</template>

<script>
import Escritores from "./components/Escritores";


export default {
  name: "app",
  components: {
    Escritores
  },
  data() {
    return {
      escritores: [],
      frases: []
    };
  },
  mounted() {
    axios
      .get("https://dataserverdaw.herokuapp.com/escritores")
      .then(response => {
        this.escritores = response.data["escritores"];
      });
    axios
      .get("https://dataserverdaw.herokuapp.com/escritores/frases")
      .then(response => {
        this.frases = response.data["frases"];
      });
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}
#app h1 {
  text-align: center;
}
</style>
