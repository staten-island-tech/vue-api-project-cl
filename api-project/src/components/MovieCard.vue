<template>
  <div class="container">

    <section id="card" class="flex">
      <div class="cover" >
      </div><!-- End of id="card" -->
      <div class="text ">
          <h1 id="title">{{mCard.director}}</h1>
          <h1 id="original-title">{{mCard.original_title}}</h1>
      </div> <!-- end of id="text" -->
      
    </section> <!-- end of id="card" -->

  </div>

</template>

<script>
export default {
    name: 'MovieCard',
    props: ["mCard"],

    methods: {
      generate() {
        console.log(`yes`)
      },
    }
}
</script>

<style scoped>
.flex {
  display: flex;
}

#card {
  justify-content: center;
  background-color: grey;
  width: 50rem;
  margin: 1rem  ;
  
}
.cover {
  /* background-image: url(https://image.tmdb.org/t/p/w600_and_h900_bestv2/39wmItIWsg5sZMyRUHLkWBcuVCM.jpg); */
}
</style>