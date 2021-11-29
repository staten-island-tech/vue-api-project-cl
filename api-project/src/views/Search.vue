<template>
  <section class="search">
    <div class="movie-box ">
      <div class="input-nav" >
        <input class="input" v-model="search" type="text" placeholder="Movie Title English">
      </div>
      <div class="temp">
        <SearchMain v-for="title in filterArray" 
        :key="title" 
        :mTitle="title"/>

      </div>

    </div>
  </section>
</template>

<script>
import SearchMain from '@/components/SearchMain.vue';
export default {
  name: `Search`,
  components: {
    SearchMain
  },
  data () {
    return {
      filterArray: [''],
      search: '',
    };
  },
  created: function () {
    this.fetchData();
    console.log(this.filterArray.title, "done")
    
  },
  methods: {
    fetchData: async function () {
      try {
        const response = await fetch (
          ////api link
          'https://ghibliapi.herokuapp.com/films'
        ); //link to the api 
        const data = await response.json(); // grabs the data (i'm guessing)
        this.filterArray = data;
        // console.log(data);
        console.log(this.filterArray);
        
      } catch (error) {
        console.log(error)
      }
    },

  },
  computed: {
      filterTitle () {
        let tempMovie = this.filterArray
    
        // Process search input
        if (this.search != '' && this.search) {
            tempMovie = tempMovie.filter((item) => {
              return item.title
                .toUpperCase()
                .includes(this.search.toUpperCase())
            })
          }
          return tempMovie
    },

  }
}


</script>

<style scoped>
.search {
  width: 100%;
  margin: auto;
}

.input-nav{
  display: flex;
  justify-content: center;
}
.input {
  border: 0.5px solid black;
  width: 20rem;
  height: 2rem;

  margin: 1rem;
  padding: 0.5rem;
  font-size: 1.5rem;

}

</style>