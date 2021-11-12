<template>
  <div class="container">

    <section id="card" class="flex">
      <div class="background"></div>
      <div class="text">
        <h1 id="title">{{title.title}}</h1>
        <h1 id="original-title">{{title.original_title}}</h1>
      </div> <!-- end of id="text" -->
    </section> <!-- end of id="card" -->

  </div>

</template>

<script>
export default {
    name: 'HomeComp',
    props: ["title"],

    methods: {
      generate() {
        console.log("completed" + this.deals )
      }
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
</style>