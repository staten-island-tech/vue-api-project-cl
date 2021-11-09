<template>
  <div class="home">
    <!-- <HomeComp v-for="item in array" :key="item" :item="deal" /> -->
    <div class="container">
      <button v-on:click="generate()" v-for="item in array" :key="item.title" >
        <h1>{{ item }}</h1>
      </button>
  </div>
  </div>
</template>

<script>
// @ is an alias to /src
// import HomeComp from '@/components/HomeComp.vue';

export default {
  name: 'Home',
  components: {
    // HomeComp,
  },
  data () {
    return {
      array: [], ///array
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
          'https://www.cheapshark.com/api/1.0/deals'
        ); //link to the api 
        const data = await response.json(); // grabs the data (i'm guessing)
        this.array = data.results; //push data into array (?)
        console.log(data);
      } catch (error) {
        console.log(error)
      }
    },
  }
}
</script>
