<style scoped>
  img {
   object-fit: cover;
   opacity: 0.7;
  }
</style>
<template>
    <div>
        <div class="card mb-3" style="max-width: 540px;">
            <div class="row no-gutters">
                <div class="col-md-4 bg-dark">
                <img class="bd-placeholder-img" width="100%" height="250" :src="anime.image_url"/>
                </div>
                <div class="col-md-8">
                <div class="card-body">
                    <h5 class="card-title">{{anime.title}}</h5>
                    <p class="card-text">It's a broader card with text below as a natural lead-in to extra content. This content is a little longer.</p>
                    <p class="card-text"><small class="text-muted">Last updated 3 mins ago</small></p>
                </div>
                </div>
            </div>
        </div>
    </div>
</template>
<script>
export default {
  name: 'AnimeCard',
  props: {
    anime: Object
  }
}
</script>