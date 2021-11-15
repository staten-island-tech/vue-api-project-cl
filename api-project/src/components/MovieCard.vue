<template>
    <section class="MovieCard-Comp" >
      <div class="text">
        <h1 id="font title">{{mCard.title}}</h1>
        <h1 id="font original-title">{{mCard.original_title}}</h1>
        <h1 id="font original-title-romanised">{{mCard.original_title_romanised}}</h1>
      </div>

    </section> <!-- end of id="card" -->


</template>

<script>
export default {
    name: 'MovieCard',
    props: ["mCard"],

}
</script>

<style scoped>
* {
  margin: 0;
  font-size: 1.5rem ;
}
.MovieCard-Comp {
  width: 15rem;
  height: 20rem;
  background-color: grey;
  /* padding: 1rem; */
  margin: 0.5rem;
}
</style>