<template>
  <div class="search">
    <SearchMain v-for="movieBox in studioGibArray" 
          :key="movieBox" 
          :mBox="movieBox" 
          />

  </div>
</template>

<script>
import SearchMain from '@/components/SearchMain.vue';


export default {
    name: `Search`,
    components :{
        SearchMain
    },
    created() {
      console.log(this.movieBox)
    },
}
</script>

<style>

</style>