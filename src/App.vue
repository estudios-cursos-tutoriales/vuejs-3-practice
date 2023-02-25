<template>
  <img alt="Vue logo" src="./assets/logo.png" />
  <!--  componente genérico: solo acepta componentes que ya este cargados o estén Registrados   -->
  <component :is="componente"></component>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";
export default {
  name: "App",
  components: {
    // Otra forma de cargar un componente es:
    // Eje: Hello: HelloWord
    HelloWorld,
  },
  data() {
    return {
      componente: "HelloWorld",
    };
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
