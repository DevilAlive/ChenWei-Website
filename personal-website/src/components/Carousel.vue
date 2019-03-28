<template>
  <div id="Carousel" class="carousel slide carousel-fade" data-ride="carousel">
    <div class="carousel-inner">
			<div style="height:100vmin;" :class="'bg-dark d-flex justify-content-center carousel-item '+[picture.id == 0 ? 'active' : '']" v-for="picture in pictures" :key="picture.id">
				<img :src="'/img/'+picture.name" :alt="picture.name" class="d-block" style="width: 100vmax">
				<div class="carousel-caption d-none d-block">
					<span class="font-weight-bold" style="font-size:3rem; text-shadow: 3px 3px #333">{{ picture.title }}</span><br />
					<span style="font-size:2rem; text-shadow: 3px 3px #333">{{ picture.words }}</span>
				</div>
			</div>
    </div>
    <a class="carousel-control-prev" href="#Carousel" role="button" data-slide="prev">
      <span class="carousel-control-prev-icon" aria-hidden="true"></span>
      <span class="sr-only">Previous</span>
    </a>
    <a class="carousel-control-next" href="#Carousel" role="button" data-slide="next">
      <span class="carousel-control-next-icon" aria-hidden="true"></span>
      <span class="sr-only">Next</span>
    </a>
  </div>
</template>

<script>
export default {
	name: 'Carousel',
	data: () => {
		return {
			pictures: [
				{id: 0, name: 'IMAG0017.jpg', title: '天地', words: '一線之隔'},
				{id: 1, name: 'IMAG0021.jpg', title: '生命', words: '永不止息'},
				{id: 2, name: 'IMAG0028.jpg', title: '自然', words: '巧奪天工'},
				{id: 3, name: 'IMAG0038.jpg', title: '智慧', words: '怡然自得'},
				{id: 4, name: 'IMAG0039.jpg', title: '氣候', words: '千變萬化'},
				{id: 5, name: 'IMAG1782.jpg', title: '歷史', words: '古色古香'}
			]
		}
	}
}
</script>
