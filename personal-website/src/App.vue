<template>
  <div id="app">
    <Nav :navNames="getAllSubId()"/>

    <main>
      <div data-spy="scroll" data-target="#navbarTarget" data-offset="0">
        <Carousel/>
        <div v-for="subject in subjects" :key="subject.id">
          <Subject :id="subject.id" :subdata="subject" />
        </div>
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
      subjects: [
        {
          id: 'About',
          title: '關於我',
          subtitle: 'Hi，你發現了這個小天地，歡迎光臨， HelloWorld ！',
          picture: require('./assets/myself.png'),
          content: '我是高雄人，畢業於國立臺北科技大學資訊工程系。<br/>大學時期學習 MVC 架構、資料分析、數位影像處理、雲端平台等技術，<br/>實作: 論壇資料搜索 (Python) 、AR應用 (Unity) 、Line機器人 (JS) 、網頁後台 (PHP) 。',
          color: 'bg-linear-gradient-orange'
        },
        {
          id: 'PTT_Bot',
          title: 'PTT Bot',
          subtitle: '給予關鍵字，幫你追蹤 Ptt 論壇相關訊息，敲響你的 Line ！<br/>[TypeScript, cheerio, Line Messaging API]',
          picture: require('./assets/PTT_Bot.png'),
          content: '運用爬蟲 (cheerio) 收集 PTT 論壇資料，並用 Webhook 與 Line API 進行通訊，收到 Line 端請求時進行回應，<br/>當設定的 timer 觸發時，更新論壇資料，減少人需要長時間關注，並且可以區分論壇各版資料，<br/>並增設提供好市多會員手冊相關資料。<br/>需要自備伺服器，暫時關閉服務',
          color: 'bg-linear-gradient-yellow'
        },
        {
          id: 'BackendSystem',
          title: '後台管理系統',
          subtitle: '運用 Laravel 與 PHP 製作公司常見使用情境的功能<br/>[Laravel, PHP, phpMyAdmin, rwd]',
          picture: require('./assets/BackendSystem.png'),
          content: '使用 Laravel 模板 (Blade) 製作網頁畫面，並運用 MVC 架構將主邏輯程式區、控制器區、與輸出畫面分為不同物件，<br/>操作 Laravel 對資料庫進行更動 (migration) ，對操作資料進行防呆與安全檢查 (Validator) ，使用 Auth 建設使用者並區分權限。',
          color: 'bg-linear-gradient-green'
        },
        {
          id: 'ARoom',
          title: 'ARoom',
          subtitle: '以 AR 角度帶入程式設計所需的技術，<br/>讓你在過程中對程式語言不再陌生！<br/>[Unity, Vuforia, C#, TCP Socket]',
          picture: require('./assets/ARoom.png'),
          content: '運用 Unity 所製成的 AR 情境，AR 採用 Vuforia 技術完成，設計結合虛實的內容，在手機上操作或是真實物品操作，<br/>為了讓多人可以一同連線，採用另外單一程式為伺服器，Server 與 Client 之間採用 TCP Socket 連線使得所有 Client 可以共享進度。',
          color: 'bg-linear-gradient-bluesky'
        },
        {
          id: 'Stick_Man_Archer',
          title: 'Stick Man Archer',
          subtitle: '有著2D與3D呈現的模式，讓喜歡挑戰的你用最快時間擊敗他。<br />此外我們還有許多不同主題場景，讓你眼花撩亂，快來挑戰吧！<br/>[Unity shader & scene, C#]',
          picture: require('./assets/stickman.png'),
          content: '運用 Unity 所製成的小遊戲，使用介面切換更換場景，有多個地形可供選擇，運用 Unity Collider 偵測碰撞，並有雙視角切換來更換第三人稱為第一人稱，增加玩家難度。',
          color: 'bg-linear-gradient-purple'
          // <a href="#">Windows - Download</a>
        }
      ]
    }
  },
  methods:{
    getAllSubId() {
      let subIds = []
      this.subjects.forEach(element => {
        subIds.push({id: element.id, name: element.title})
      });
      return subIds
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
  height: 50vmin;
}
.bg-linear-gradient-orange {
  background: linear-gradient(to bottom right, #ffbb33 0, #ff2233 100%);
}
.bg-linear-gradient-bluesky {
  background: linear-gradient(to bottom right, #77bbff 0, #55eeff 100%);
}
.bg-linear-gradient-green {
  background: linear-gradient(to bottom right, #00aa11 0, #55ff22 100%);
}
.bg-linear-gradient-yellow {
  background: linear-gradient(to bottom right, #ffee33 0, #eeee77 100%);
}
.bg-linear-gradient-purple {
  background: linear-gradient(to bottom right, #bb77ff 0, #6644ff 100%);
}
</style>
