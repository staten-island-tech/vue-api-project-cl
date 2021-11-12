<template>
  <div class="home">

    <HomeComp v-for="title in studioGibArray" :key="title" :title="title" />
    
  </div>

</template>

<script>
// @ is an alias to /src
import HomeComp from '@/components/HomeComp.vue';

export default {
  name: 'Home',
  components: {
    HomeComp,
  },
  data () {
    return {
      studioGibArray: [], ///array
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
