<template>
  <nav id="navbarTarget" class="navbar navbar-expand-lg sticky-top navbar-dark bg-primary">
    <div class="container">
      <a href="#" class="navbar-brand">ChenWei-MO</a>
      <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>

      <div class="collapse navbar-collapse" id="navbarSupportedContent">
        <ul class="navbar-nav justify-content-between">
          <li class="nav-item" v-for="navName in navNames" :key="navName.id">
            <a :href="`#${navName.id}`" class="nav-link">{{ navName.name }}</a>
          </li>
        </ul>
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  id: "Nav",
  props: ['navNames'],
  data: () => {
    return {}
      // navNames: [{ id: "Carousel", name: "活動" }, { id: "About", name: "關於我" }, { id: "Subject1", name: "項目1" }]
  }
};
</script>
