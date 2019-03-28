<template>
  <nav id="navbarTarget" class="navbar navbar-expand-lg fixed-top navbar-dark bg-primary">
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
          <li class="nav-item" :key="navName.name" v-for="navName in navNames">
            <a :href="'#'+navName.name" class="nav-link">{{ navName.name }}</a>
          </li>
        </ul>
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  name: 'Nav',
  data: () => {
    return {
      navNames: [{ name: "Carousel" }, { name: "VueLogo" }, { name: "helloWorld1" }, { name: "helloWorld2" }, { name: "helloWorld3" }, { name: "helloWorld4" }]
    };
  }
};
</script>
