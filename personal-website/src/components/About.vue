<template>
  <div class="bg-linear-gradient-orange">
    <div class="container">
      <div class="blockHeight d-flex flex-column justify-content-center align-items-center">
        <div class="d-flex align-items-center">
          <div class="d-flex flex-column" style="width: 60%">
            <span class="ml-auto" style="font-size: 1.5rem">關於我</span>
            <p class="text-wrap" style="font-size: 1.1rem">Hi，你發現了這個小天地，你真的很棒，誒不是，不要關掉網頁拉～</p>
          </div>
          <img src="../assets/logo.png" alt="About" style="padding: 10px; width: 40vmin; height: 40vmin"/>
        </div>
        <button class="btn btn-outline-light" type="button" data-toggle="collapse" data-target="#aboutCollapse" aria-expanded="false" aria-controls="aboutCollapse">檢視更多</button>
      </div>
      <div class="collapse pb-5" id="aboutCollapse">
        <div class="card card-body bg-dark">
          <p>安安，我是高雄人，人生志向還在尋找，不希望急著定義自我，人生晚長，期望過著與朋友鬼混的生活，但實際上習慣一個人過活，常常到處亂晃，不過有事情有興趣就會毛起來弄，有點廢寢忘食。</p>
          <span>2019年05月01日 莫鎮瑋</span>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "About",
  data() {
    return {}
  },
  methods: {
    gogogo() {}
  },
};
</script>

<style>
</style>

