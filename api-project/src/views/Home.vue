<template>
  <div class="home">

    <MovieCard v-for="movieCard in studioGibArray" :key="movieCard" :mCard="movieCard" />
    
  </div>

</template>

<script>
// @ is an alias to /src
import MovieCard from '@/components/MovieCard.vue';

export default {
  name: 'Home',
  components: {
    MovieCard,
  },
  data () {
    return {
      studioGibArray: [''], ///array
      cover: [''], ///array
    };
  },
  created: function () {
    this.fetchData();
  },
  methods: {
    fetchData: async function () {
      try {
        const response = await fetch (
          ////api link
          'https://ghibliapi.herokuapp.com/films'
        ); //link to the api 
        const data = await response.json(); // grabs the data (i'm guessing)
        this.studioGibArray = data; //push data into array (?)
        // console.log(data);
        console.log(this.studioGibArray);
      } catch (error) {
        console.log(error)
      }
    },

  }
}
</script>
