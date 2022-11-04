<template>
  <v-main>
    <section class="carousel-section">
      <carousel />
    </section>
    <section class="card">
      <!--Card 1-->
      <div class="card__container">
        <div class="card__text">
          <h2>First featurette heading. <span class="">It’ll blow your mind.</span></h2>
          <p>Some great placeholder content for the first featurette here. Imagine some exciting prose here.</p>
          <a href="#" class="buttons__anchor">Saiba mais...</a>
        </div>
        <div class="card__space-img">
          <img class="card__img" src="../assets/img/500x500/01.jpg" alt="">
        </div>
      </div>
      <hr />
      <!--Card 2-->
      <div class="card__container">
        <div class="card__space-img">
          <img class="card__img" src="../assets/img/500x500/02.jpg" alt="">
        </div>
        <div class="card__text">
          <h2>Oh yeah, it’s that good. <span class="">See for yourself.</span></h2>
          <p>Another featurette? Of course...</p>
          <a href="#" class="buttons__anchor">Saiba mais...</a>
        </div>
      </div>
      <hr />
      <!--Card 3-->
      <div class="card__container">
        <div class="card__text">
          <h2>And lastly, this one. <span class="">Checkmate.</span></h2>
          <p>And yes, this is the last block of representative placeholder content. Again, not really intended to be
            actually read.</p>
          <a href="#" class="buttons__anchor">Saiba mais...</a>
        </div>
        <div class="card__space-img">
          <img class="card__img" src="../assets/img/500x500/03.jpg" alt="">
        </div>
      </div>
    </section>
  </v-main>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import Carousel from '../components/Carousel.vue';



export default defineComponent({
  name: 'HomeView',
  components: {
    Carousel,
    
  },
});
</script>

<style lang="scss" scoped>
.carousel-section {
  display: inline-block;
  width: 100%;
  padding-top: 6.25rem;
}

.card{
    display: inline-block;
    margin-top: 5em;
    width: 100%;
    
}

.card__container{
    display: flex;
    justify-content: space-between;
    margin: 3em 0;
    padding: 2em;
    border: 1px solid var(--shadow);
    border-radius: 6px;
    background: var(--background-color-dark-white);
    box-shadow: 10px 7px 5px rgba(0, 0, 0, 0.290);

} 

.card__text{
    text-align: center;
    position: relative;
    margin: auto;
    font-family: var(--cartoon-font);
}



.card__img{
    width: 300px;
    height: 300px;
    border-radius: 10px;
    box-shadow: 10px 7px 5px rgba(0, 0, 0, 0.295);
}

.buttons__anchor{
    background-color: var(--light-blue);
    padding: 1em 2.2em;
    text-align: center;
    margin-top: 2em;
    color: var(--white);
    font-weight: 700;
    text-decoration: none;
    border-radius: 6px;
    display: inline-block;
}

.buttons__anchor:hover{
    transform: scale(1.20);
    background-color: blue;
}
</style>
