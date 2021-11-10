<template>
  <div class="container">
    <h1>{{title.title}}</h1>
  </div>
</template>

<script>
export default {
    name: 'HomeComp',
    props: ["title"],
    ///computed Property == 
    methods: {
      generate() {
        console.log("completed" + this.deals )
      }
    }
}
</script>

<style>

</style>