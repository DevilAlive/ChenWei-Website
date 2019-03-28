<template>
  <div id="app">
    <Nav/>
    <div data-spy="scroll" data-target="#navbarTarget" data-offset="0">
      <Carousel/>
      <div id="VueLogo" class="bg-warning d-flex align-items-center justify-content-center" style="height: 60vh;">
        <img alt="Vue logo" src="./assets/logo.png">
      </div>
			<HelloWorld msg="Welcome to Your Vue.js App"/>
    </div>
    <br>
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";
import Nav from "./components/Nav.vue";
import Carousel from "./components/Carousel.vue";

export default {
  name: "app",
  components: {
    HelloWorld,
    Nav,
    Carousel
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  /* margin-top: 60px; */
}
</style>
