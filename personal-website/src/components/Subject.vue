<template>
  <div class="bg-linear-gradient-bluesky">
    <div class="container">
      <div class="blockHeight d-flex flex-column justify-content-center align-items-center">
				<div class="d-flex align-items-center">
					<div class="d-flex flex-column" style="width:60%">
						<span class="ml-auto" style="font-size: 1.5rem;">Sticky Man</span>
						<p class="text-wrap" style="font-size: 1.1rem;">運用 Unity 所製成的小品遊戲</p>
					</div>
          <img src="../assets/logo.png" alt="About" style="padding:10px; width:40vmin; height:40vmin;">
				</div>
        <button class="btn btn-outline-light" type="button" data-toggle="collapse" data-target="#subjectCollapse" aria-expanded="false" aria-controls="subjectCollapse">檢視更多</button>
			</div>
			<div class="collapse pb-5" id="subjectCollapse">
				<div class="card card-body bg-dark">
					<p>火柴人的對決，快來擊敗電腦人，有著2D與3D呈現的模式，讓喜歡挑戰的你用最快時間擊敗他。<br />
					此外我們還有許多不同主題場景，讓你眼花撩亂，快來挑戰吧！</p>
					<a href="#">Windows - Download</a>
				</div>
			</div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Subject",
  data() {
    return {}
  }
};
</script>
