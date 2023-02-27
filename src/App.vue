<template>
  <img alt="Vue logo" src="./assets/logo.png" />
  <div class="container my-4">
    <button class="btn btn-primary btn-block" @click="show = !show">Our Gallery</button>
  </div>
  <transition name="fade">
    <Gallery v-show="show"></Gallery>
  </transition>
</template>

<script>
import Gallery from "./components/Gallery.vue";
export default {
  name: "App",
  components: {
    Gallery,
  },
  data(){
    return {
      show: false,
    }
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
.fade-enter-from,
.fade-leave-to{
  opacity: 0;
}

.fade-leave-active,
.fade-enter-active{
  transition: opacity 0.5s ease;
}
</style>
