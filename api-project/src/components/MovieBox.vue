<template>
  <section id="MovieBox" class="flex-center">
      <div class="main">
          <div class="text">

            <div class="flex-col top">
                <div class="flex-row">
                    <img :src="mBox.image" alt="" class="cover top-left">

                    <div class="flex-col top-right">
                        <div class="title">
                                <h1 class="font eng-title">{{mBox.title}}</h1> 
                                <h2 class="font original-title-romanised">{{mBox.original_title_romanised}}</h2>
                                <h1 class="font original-title">{{mBox.original_title}}</h1>
                                
                            </div>
                            <div class="people">
                                <h3>Director: {{mBox.director}} </h3>
                                <h3>Producer: {{mBox.producer}}</h3>
                            </div>

                            <div class="other">
                                <h4>RT Score: {{mBox.rt_score}}</h4>
                                <h4>Released: {{mBox.release_date}}</h4>
                                <h4>Time: {{mBox.running_time}} minutes</h4>
                            </div>
                    </div>
                </div>
                
            </div> <!-- end of "top" -->

            <div class="flex-col btm">
                <p class="summary">{{mBox.description}}</p>
            </div>
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

}
</script>

<style lang="css" scoped>
.flex-center  {
    display: flex;
    align-content: center;
    justify-content: center;
}
#MovieBox {
    width: 100rem;
    height: auto;
    background-color: grey;
    padding-top: 3rem;

    font-size: 2rem;

}
.main  {
    width: 75%;
    padding-bottom: 3rem;
    border-bottom: 1px black solid;
}

.flex-col {
    display: flex;
    flex-direction: column;
}
.flex-row {
    display: flex;
    flex-direction: row;
}
.cover {
    height: 40rem;
    background-color: black;
}

.font{
    font-size: 1rem;
}
.title {
    padding-bottom: 1rem;
}
.people {
    padding-bottom: 1rem;
}
</style>