<template>
  <section id="search">
     <div class="box-container" :style={}>

       <div class="text-main" >
         <div class="titles">
          <h1 class="title-eng">{{mTitle.title}}</h1>
          <h1 class="title-rom">{{mTitle.original_title_romanised}}</h1>
          <h1 class="title-orig">{{mTitle.original_title}}</h1>
         </div> <!-- end of title -->
         <div class="people">
           <h2 class="director">Director: {{mTitle.director}}</h2>
           <h2 class="producer">Producer(s): {{mTitle.producer}}</h2>
         </div>
       </div> <!-- end of text-main -->

       <div class="text-sub">
         <p class="description">
           {{mTitle.description}}
         </p>
       </div> <!-- end of text-sub -->

     </div> <!-- end of box-container -->
  </section>
</template>

<script>

export default {
    name: "SearchMain",
    props: ["mTitle"],
    components: {

  },
}
</script>

<style>
#search {
  display: flex;
  justify-content: center;
}

.box-container {
  max-width: 50rem;
  border: solid 1px black;
}

.text-main {
  background-color: red;
}
.titles {
  background-color: grey;
}
.people {
  background-color: whitesmoke;
}

.text-sub {
  background-color: blue;
}
.description {
  background-color: wheat;
}
</style>