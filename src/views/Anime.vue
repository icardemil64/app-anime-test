<template>
    <div class="container">
        <div class="row">
            <div v-for="(item,index) in animes.anime" :key="index" class="col-6">
                <AnimeCard :anime = "item"/>
            </div>
        </div>
    </div>
</template>
<script>
import AnimeCard from '@/components/AnimeCard'
export default {
    components:{
        AnimeCard,
    },
    data() {
        return {
            animes : [],
            season: this.$route.params.season,
            anio: this.$route.params.anio,
        }
    },
    created() {
        this.getAnime(this.season);
    },
    methods: {
        getAnime(season){
            this.axios.get(`/season/${this.anio}/${this.season}`)
             .then(res => {
                 this.animes = res.data;
                 console.log(this.animes.anime);
             })
              .catch(e => {
                  console.log(e.response)
              })
        }
    },
}
</script>