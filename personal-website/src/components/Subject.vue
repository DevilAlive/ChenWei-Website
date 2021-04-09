<template>
  <div :class="subdata.color">
    <div class="container smooth">
      <div class="blockHeight d-flex flex-column justify-content-center align-items-center">
        <div class="d-flex align-items-center">
          <div class="d-flex flex-column" style="width: 60%">
            <span class="ml-auto" style="font-size: 1.5rem">{{ subdata.title }}</span>
            <p class="text-wrap" style="font-size: 1.1rem">{{ subdata.subtitle }}</p>
          </div>
          <img :src="subdata.picture" alt="About" style="padding: 10px; width: 40vmin; height: 40vmin"/>
        </div>
        <button class="btn btn-outline-light" type="button" data-toggle="collapse" :data-target="`#${subdata.id}Collapse`" aria-expanded="false" :aria-controls="`${subdata.id}Collapse`">檢視更多</button>
      </div>
      <div class="collapse pb-5" :id="`${subdata.id}Collapse`">
        <div class="card card-body bg-dark">
          <p v-html="subdata.content"></p>
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
