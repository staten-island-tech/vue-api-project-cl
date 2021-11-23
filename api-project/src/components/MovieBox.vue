<template>
  <section id="MovieBox">
      <div class="main">
          <div class="text">
            <h1 class="font original-title">{{mBox.original_title}}</h1>
            <h1 class="font original-title-romanised">{{mBox.original_title_romanised}}</h1>
            <h1 class="font eng-title">{{mBox.title}}</h1> 
            
            <p class="summary">{{mBox.description}}</p>
        </div>
      </div>
  </section>
</template>

<script>
export default {
    name: 'MovieBox',
    props: ["mBox"],
    data() {
        return {
        }
    },
    created() {
        console.log(this.mBox)
        
    },
    methods: {
        changeProd() {
            // if (mBox.producer.length >= 1) {
                
            // } else {
                
            // }
        },
    }

}
</script>

<style lang="css" scoped>

#MovieBox {
    width: 100rem;
    height: 100rem;
    background-color: grey;

}
</style>