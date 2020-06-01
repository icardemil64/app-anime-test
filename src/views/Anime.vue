<template>
    <div class="container">
        <form class="form-inline" @submit.prevent="getAnime(id)">
            <input type="number" class="form-control my-2" placeholder="Ingresa ID" v-model="id">
            <button class="btn btn-warning my-2 mx-2" type="submit">Buscar serie</button>
        </form>
        <h1>{{anime.title}}</h1>
        <img :src="anime.image_url">
        <h5>{{anime.title_english}}</h5>
        <h5>{{anime.title_japanese}}</h5>
        <iframe id="player" type="text/html" width="640" height="360"
                :src="anime.trailer_url"
                frameborder="0">
        </iframe>
    </div>
</template>
<script>
export default {
    data() {
        return {
            anime : {},
            id: 1
        }
    },
    created() {
        this.getAnime(this.id);
    },
    methods: {
        getAnime(id){
            this.axios.get(`/anime/${this.id}`)
             .then(res => {
                 console.log(res.data)
                 this.anime = res.data;
             })
              .catch(e => {
                  console.log(e.response)
              })
        }
    },
}
</script>