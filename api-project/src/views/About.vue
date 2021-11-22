<template>
  <section>
    <MovieBox v-for="movieBox in studioGibArray" 
          :key="movieBox" 
          :mBox="movieBox" />
  </section>
</template>

<script>
import MovieBox from '@/components/MovieBox.vue';
 
export default {
  name: 'About',
  components: {
    MovieBox,
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

  }
}
</script>

<style>

</style>