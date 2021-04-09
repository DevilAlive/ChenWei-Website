<template>
  <div id="app">
    <Nav :navNames="getAllSubId()"/>

    <main>
      <div data-spy="scroll" data-target="#navbarTarget" data-offset="0">
        <Carousel/>
        <Subject :id="about.id" :subdata="about" />
        <Subject :id="subject1.id" :subdata="subject1" />
        <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
      </div>
    </main>

    <Footer/>
  </div>
</template>

<script>
import Nav from "./components/Nav.vue"
import Carousel from "./components/Carousel.vue"
import Subject from "./components/Subject.vue"
import Footer from "./components/Footer.vue"

export default {
  name: "app",
  components: {
    Nav,
    Carousel,
    Subject,
    Footer
  },
  data() {
    return {
      about: {
        id: 'About',
        title: '關於我',
        subtitle: 'Hi，你發現了這個小天地，你真的很棒，誒不是，不要關掉網頁拉～',
        picture: require('./assets/logo.png'),
        content: '安安，我是高雄人，人生志向還在尋找，不希望急著定義自我，人生晚長，期望過著與朋友鬼混的生活，但實際上習慣一個人過活，常常到處亂晃，不過有事情有興趣就會毛起來弄，有點廢寢忘食。<br /><span>2019年05月01日 莫鎮瑋</span>',
        color: 'bg-linear-gradient-orange'
      },
      subject1: {
        id: 'Subject1',
        title: 'Sticky Man',
        subtitle: '運用 Unity 所製成的小品遊戲',
        picture: require('./assets/logo.png'),
        content: '火柴人的對決，快來擊敗電腦人，有著2D與3D呈現的模式，讓喜歡挑戰的你用最快時間擊敗他。<br />此外我們還有許多不同主題場景，讓你眼花撩亂，快來挑戰吧！<br /><a href="#">Windows - Download</a>',
        color: 'bg-linear-gradient-bluesky'
      }
    }
  },
  methods:{
    getAllSubId() {
      return [
        {id: this.about.id, name: this.about.title},
        {id: this.subject1.id, name: this.subject1.title},
      ]
    }
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
