<template>
  <div class="home">
    <HomeComp />
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
      dndArray: [], ///array
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
          'www.dnd5eapi.co/api/'
        ); //link to the api 
        const data = await response.json(); // grabs the data (i'm guessing)
        this.dndArray = data.results; //push data into array (?)
        console.log(data);
      } catch (error) {
        console.log(error)
      }
    },
  }
}
</script>
