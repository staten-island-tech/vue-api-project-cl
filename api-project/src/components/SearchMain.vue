<template>
  <section id="search">
     <div class="box-container" :style="{backgroundImage:`url(${mTitle.movie_banner})`}">

       <div class="text-main flex-row" >
         <div class="left">
           <div class="titles">
              <h1 class="title-font title-eng">{{mTitle.title}}</h1>
              <h1 class="title-font title-rom">{{mTitle.original_title_romanised}}</h1>
              <h1 class="title-font title-orig">{{mTitle.original_title}}</h1>
            </div> <!-- end of title -->
         </div>

         <div class="right">
          <div class="people">
            <h2 class="people-font director">Director: {{mTitle.director}}</h2>
            <h2 class="people-font producer">Producer(s): {{mTitle.producer}}</h2>
            <h3 class="time-font time">Watch Time: {{mTitle.running_time}} minutes</h3>
            <h3 class="time-font rekease">Released in {{mTitle.release_date}}</h3>
          </div><!-- end of people -->
         </div>
       </div> <!-- end of text-main -->

       <div class="text-sub">
         <p class="description">
           {{mTitle.description}}
         </p>
       </div> <!-- end of text-sub -->

       <div class="url flex-col-center">
         <h3 class="api-url">API Url (It's not an "a" tag)</h3>
         <h3 class="api-url"> {{mTitle.url}}</h3>
       </div>

     </div> <!-- end of box-container -->
  </section>
</template>

<script>

export default {
    name: "SearchMain",
    props: ["mTitle"],
}
</script>

<style>
.flex-row {
  display: flex;
  flex-direction: row;
}
.flex-col-center {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
#search {
  display: flex;
  justify-content: center;
  
  margin: auto;
  color: white;
  margin: 1.5rem 0;
}

.box-container {
  max-width: 50rem;
  border: solid 1px black;
  padding: 1.5rem ;
  
  background-size: cover;
  background-repeat: no-repeat;
}

.text-main {
  background-color: rgba(0, 0, 0, 0.8);
  margin: 1rem;
  padding: 1rem;
}
.title-font {
  font-size: 1.5rem;
}
.left{
  width: 60%;
  padding-right: 1rem;
}

.text-sub {
  background-color: rgba(0, 0, 0, 0.8);
  margin: 1rem;
  padding: 1.5rem;
}
.people-font {
  font-size: 1rem;
  font-weight: 400;

  color: rgb(224, 211, 211);
}
.time-font {
  font-size: 1rem;
  font-weight: 400;

  color: rgb(185, 211, 178);
}

.description {
  font-size: 1.5rem;
  font-weight: 200;
}

.url{
  display: flex;
  justify-content: center;
  align-content: center;

  min-width: 1rem;
  padding: 0.5rem;
  background-color: rgba(252, 239, 253, 0.795);
}
.api-url  {
  font-size: 1rem;
  font-weight: 400;
  color: rgb(0, 0, 0);
}
</style>