<template>
  <div id="app">
    <Nav/>

    <main>
      <div data-spy="scroll" data-target="#navbarTarget" data-offset="0">
        <Carousel/>
        <About id="About"/>
        <Subject id="Subject"/>
        <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
      </div>
    </main>

    <Footer/>
  </div>
</template>

<script>
import Nav from "./components/Nav.vue"
import Carousel from "./components/Carousel.vue"
import About from "./components/About.vue"
import Subject from "./components/Subject.vue"
import Footer from "./components/Footer.vue"

export default {
  name: "app",
  components: {
    Nav,
    Carousel,
    About,
    Subject,
    Footer
  }
};
</script>


<style>
@font-face {
  font-family: "Noto Sans CJK TC";
  src: url("./assets/font/NotoSansCJKtc-Regular.otf") format("opentype");
}
#app {
  /* font-family: "Avenir", Helvetica, Arial, sans-serif; */
  font-family: "Noto Sans CJK TC";
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  /* margin-top: 60px; */
}
img {
  filter: drop-shadow(1rem 1rem 1.1rem #333333);
}
span,
p {
  color: white;
  text-shadow: 1rem 1rem 1.1rem #333333;
}
button {
  text-shadow: 1rem 1rem 1.1rem #333333;
}
.smooth {
  transition: all 1s;
}
.blockHeight {
  height: 60vh;
}
.bg-linear-gradient-orange {
  background: linear-gradient(to bottom right, #ffbb33 0, #ff2233 100%);
}
.bg-linear-gradient-bluesky {
  background: linear-gradient(to bottom right, #77bbff 0, #55eeff 100%);
}
</style>
