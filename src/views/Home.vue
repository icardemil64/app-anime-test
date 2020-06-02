<template>
  <div class="container">
    <div class="row">
      <div v-for="(item,index) in seasons" :key="index" class="col-6">
        <SeasonCard :season="item"/>
      </div>
    </div>
  </div>
</template>

<script>
  import SeasonCard from '@/components/SeasonCard'
  export default{
    components:{
        SeasonCard,
    },
    data() {
      return {
        seasons:[
          { nombre:'Verano',
            img: 'https://res.cloudinary.com/jerrick/image/upload/q_auto,w_720/z0vsuudaaausognyzzhd.jpg',
            anio: 2015,
            name: 'summer'},
          { nombre:'Primavera',
            img: 'https://cdn.myanimelist.net/s/common/uploaded_files/1576984390-46c7bde42abd3425ebc3aa79a33efa20.jpeg',
            anio: 2015,
            name: 'spring'},
          { nombre:'Invierno',
            img: 'https://3.bp.blogspot.com/-_hUBQp7xmpk/Ub6kM1KUaxI/AAAAAAAAAV4/ibdT2Ybyi7I/s1600/winter_sonata2.jpg',
            anio: 2015,
            name: 'winter'},
          { nombre:'Otoño',
            img: 'https://d1a2e1vehwcxq9.cloudfront.net/news/2017/02/anime-background-art-beautiful-bones-2.jpg',
            anio: 2015,
            name: 'fall'}]
      }
    },
  }
</script>
