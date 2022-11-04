<template>
  <v-main>
    <!-- Carrosel -->
    <section class="carousel-section">
      <carousel/>
    </section>
    <!--Cards -->
    <section class="card-section">
      <div class="card">
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
        <hr />
        <!--Card 4-->
        <div class="card__container">
          <div class="card__space-img">
            <img class="card__img" src="../assets/img/500x500/01.jpg" alt="">
          </div>
          <div class="card__text">
            <h2>Oh yeah, it’s that good. <span class="">See for yourself.</span></h2>
            <p>Another featurette? Of course...</p>
            <a href="#" class="buttons__anchor">Saiba mais...</a>
          </div>
        </div>
        <hr />
        <!--Card 5-->
        <div class="card__container">
          <div class="card__text">
            <h2>And lastly, this one. <span class="">Checkmate.</span></h2>
            <p>And yes, this is the last block of representative placeholder content. Again, not really intended to be
              actually read.</p>
            <a href="#" class="buttons__anchor">Saiba mais...</a>
          </div>
          <div class="card__space-img">
            <img class="card__img" src="../assets/img/500x500/02.jpg" alt="">
          </div>
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
.card-section{
  margin-left: auto;
  margin-right: auto;
  width: 80%;
  justify-items: center;
}
.card {
  display: inline-block;
  justify-items: center;
  margin-top: 1em;
  width: 100%;

  hr{
    margin: -1rem 0;
    border-color: rgba(0, 0, 0, 0.781);
  }
  .card__container {
    display: flex;
    justify-content: space-between;
    margin: 3em 0;
    padding: 2em;
    border: 1.5px solid var(--shadow);
    border-radius: 6.8px;
    background: var(--background-color-dark-white);
    box-shadow: 10px 7px 5px rgba(0, 0, 0, 0.290);

  }
  .card__text {
    text-align: center;
    position: relative;
    margin: auto;
    color: black;
    font-family: var(--cartoon-font);
    font-weight: 500;
    font-size: 16px;

    h2{
      font-weight: 700;
      font-size: 18px;

      span{
        color: gray;
      }
    }

  }
  .card__img {
    width: 300px;
    height: 300px;
    border-radius: 10px;
    box-shadow: 10px 7px 5px rgba(0, 0, 0, 0.295);
  }
  .buttons__anchor {
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
  .buttons__anchor:hover {
    transform: scale(1.20);
    background-color: blue;
  }
}
</style>
