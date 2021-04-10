<template>
  <div :class="subdata.color">
    <div class="container smooth">
      <div class="py-5 d-flex flex-column justify-content-center align-items-center">
        <div class="d-flex align-items-center">
          <div class="d-flex flex-column">
            <span class="ml-auto" style="font-size: 2rem">{{ subdata.title }}</span>
            <p class="text-wrap" v-html="subdata.subtitle"></p>
          </div>
          <img :src="subdata.picture" alt="About" class="p-2" style="border-radius: 40px; height: 30vmin"/>
        </div>
        <button class="btn btn-outline-light my-3" type="button" data-toggle="collapse" :data-target="`#${subdata.id}Collapse`" aria-expanded="false" :aria-controls="`${subdata.id}Collapse`">檢視更多</button>
        <div class="collapse py-3" :id="`${subdata.id}Collapse`">
          <div class="card card-body bg-dark">
            <p class="m-0" v-html="subdata.content"></p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Subject",
  props: ['subdata'],
  data() {
    return {}
    // subdata: {id: '', title: '', subtitle: '', picture: '', content: '', color: ''}
  }
};
</script>
