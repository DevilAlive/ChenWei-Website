<template>
  <nav id="navbarTarget" class="navbar navbar-expand-lg sticky-top navbar-dark bg-primary">
    <div class="container">
      <a href="#" class="navbar-brand">SmallMO</a>
      <button
        class="navbar-toggler"
        type="button"
        data-toggle="collapse"
        data-target="#navbarSupportedContent"
        aria-controls="navbarSupportedContent"
        aria-expanded="false"
        aria-label="Toggle navigation"
      >
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
  data: () => {
    return {
      navNames: [
        { id: "Carousel", name: "活動" },
        { id: "VueLogo", name: "關於我" },
        { id: "helloWorld1", name: "項目1" },
        { id: "helloWorld2", name: "項目2" },
        { id: "helloWorld3", name: "項目3" },
        { id: "helloWorld4", name: "項目4" }
      ]
    };
  }
};
</script>
