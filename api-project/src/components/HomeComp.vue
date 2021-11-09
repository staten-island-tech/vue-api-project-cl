<template>
  <div class="container">
      <button v-on:click="generate()" >
        <h1>{{deal.title}}</h1>
      </button>
  </div>
</template>

<script>
export default {
    name: 'HomeComp',
    props: ["deals"],
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