<template>
    <section id="MovieCard-Comp" class="flex-col">
      <img :src="mCard.image" alt="" class="movie-img">

      <div class="text  hover">
        <h1 class="font original-title">{{mCard.original_title}}</h1>
        <h1 class="font original-title-romanised">{{mCard.original_title_romanised}}</h1>
        <h1 class="font eng-title">{{mCard.title}}</h1>
        
      </div>

    </section> <!-- end of id="card" -->


</template>

<script>
export default {
    name: 'MovieCard',
    props: ["mCard"],
    // created() {
    //   console.log(this.mCard)
    // },

}
</script>

<style scoped>
* {
  margin: 0;

}
.flex-col {
  display: flex;
  flex-direction: column;

}

#MovieCard-Comp {
  width: 12rem;
  height: auto;

  
  margin: 1rem 0.5rem;
  background-size: cover;
}

.movie-img{
  width: 12rem;
  height: 18rem;
  background-color: rgb(199, 190, 190);
}
.text {
  display: flex;
  flex-direction: column-reverse;
  color: rgb(241, 225, 214);
  padding: .5rem 0;
}
.font {
  font-size: 1.5rem;
  font-weight: 400;
  line-height: 1.75rem;
}
.original-title-romanised {
  font-size: 1.1rem;
  line-height: 1.3rem;
  font-weight: 200;
  padding: 0.2rem 0 ;
}

</style>