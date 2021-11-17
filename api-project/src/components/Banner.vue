<template>
  <section id="Banner">
      <div class="main">
          
      </div>
  </section>
</template>

<script>
export default {
     name: 'Banner',
    props: ["banner"],
}
</script>

<style>
#Banner {
    width: 100%;
    height: 50rem;
    
}
.main {
    width: 100%;
    height: 100%;
    background-size: cover;
    background-image: url(https://image.tmdb.org/t/p/original/etqr6fOOCXQOgwrQXaKwenTSuzx.jpg);
    
}
</style>