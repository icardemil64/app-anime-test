<style scoped>
  img {
   object-fit: cover;
   opacity: 0.5;
  }
</style>

<template>
    <div id="tarjeta">
      <router-link :to="{name: 'Anime', params:{anio:season.anio,season:season.name}}">
        <div class="card bg-dark text-white mb-3" style="width: 470px">
            <img class="card-img" :src=season.img width="100%" height="290">
            <div class="card-img-overlay">
              <div class="container h-100">
                <div class="row align-items-center h-100">
                  <div class="col-6 mx-auto">
                      <h5 class="card-title">{{season.nombre}}</h5>
                  </div>
                </div>
              </div>
            </div>
        </div>
      </router-link>
    </div>
</template>
<script>
export default {
  name: 'SeasonCard',
  props: {
    season: Object
  }
}
</script>
