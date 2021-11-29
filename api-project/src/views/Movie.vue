<template>
  <section class="home display">
    <div id="movie" class="flex-col">
      <div class="movie-card flex-row-wrap flex-center">
        <MovieCard v-for="movieCard in studioGibArray" 
          :key="movieCard" 
          :mCard="movieCard" 
          />
      </div>
    </div> <!-- movie end -->
  </section>
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
  },
}
</script>

<style scoped>
.none {
  display: none;
}

.display {
  display: inline-block;
}

.flex-center {
  display: flex;
  justify-content: center;
  align-content: center;
}
.flex-row-wrap {
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
}
.flex-col {
  display: flex;
  flex-direction: column;
}

.home{
  width: 100%;
  width: 100%;
  margin: 0 auto;
  padding: 0;
}

#movie {
  width: 100%;
}
.movie-card {
  background-color: black;
  width: 100%;
  max-width: 80rem;
  margin: auto;
}

</style>