<template>
    <section id="MovieCard-Comp" class="flex" >

      <div class="text flex-col hover">
        <h1 id="font original-title">{{mCard.original_title}}</h1>
        <h1 id="font original-title-romanised">{{mCard.original_title_romanised}}</h1>
        <h1 id="font title">{{mCard.title}}</h1>
        
      </div>

    </section> <!-- end of id="card" -->


</template>

<script>
export default {
    name: 'MovieCard',
    props: ["mCard"],
    data () {
      return {
        cover: [``],
      };
    },
    created() {
      this.cover = this.mCard.image;
      console.log(this.cover)
    },

}
</script>

<style scoped>
* {
  margin: 0;
  font-size: 1.5rem ;

}
.flex {
  display: flex;
}

#MovieCard-Comp {
  width: 12rem;
  height: 18rem;
  background-color: grey;
  /* padding: 1rem; */
  margin: 0.5rem;
  background-size: cover;
  background-image: url(https://image.tmdb.org/t/p/w600_and_h900_bestv2/mikKSEdk5kLhflWXbp4S5mmHsDo.jpg);
}
.text {
  display: flex;
  flex-direction: column-reverse;
}
</style>