<template>
    <section>
      <div v-on:click="updateMain() ; changeCard2()"  id="MovieCard-Comp" class="none flex-col ">
        <img :src="mCard.image" alt="" class="movie-img">
        <div class="text">
          <h1 class="font original-title">{{mCard.original_title}}</h1>
          <h1 class="font original-title-romanised">{{mCard.original_title_romanised}}</h1>
          <h1 class="font eng-title">{{mCard.title}}</h1>
        </div> <!-- end of text-->
      </div> <!-- end of MovieCard-Comp-->

    </section>


</template>

<script>
export default {
    name: 'MovieCard',
    props: ["mCard"],
    data() {
        return {
          Main: {
            clicked: false,

            orgTitle: '',
            engTitle: '',
            romTitle: '',

            director: '',
            producer:'',

            time: '',
            released: '',

            description: '',
            banner: '',
            apiUrl:'',
            
          },
        }
    },
    created() {
      // console.log(this.mCard)
    },
    methods: {
      updateMain () {
        this.Main.orgTitle = this.mCard.original_title
        this.Main.engTitle = this.mCard.title
        this.Main.romTitle = this.mCard.original_title_romanised

        this.Main.director = this.mCard.director
        this.Main.producer = this.mCard.producer

        this.Main.time = this.mCard.running_time
        this.Main.released = this.mCard.release_date

        this.Main.description = this.mCard.description
        this.Main.banner = this.mCard.movie_banner
        this.Main.apiUrl = this.mCard.url
        console.log(this.Main)
      },
      
      changeCard2() {
        if (this.Main.clicked === false) {
          this.Main.clicked = true
          console.log(this.Main.clicked)
        } else {
          console.log('Error')
        }
      },
      
    }

}
</script>

<style scoped>
.none {
  display: none;
}
.display {
  display: inline-block;
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
#MovieCard-Comp:hover {
  text-decoration: underline 1px rgb(133, 133, 133);
  cursor: pointer;
  text-underline-position: under;
}

.movie-img{
  width: 12rem;
  height: 18rem;
  background-color: grey;
}

.text {
  display: flex;
  flex-direction: column-reverse;
  color: rgb(241, 225, 214);
  margin: .5rem 0;
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