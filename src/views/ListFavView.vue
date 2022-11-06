<template>
    <v-main>
      <section class="card-section">
        <div class="card">
          <div class="card__container">
            <div class="card__space-img">
              <img class="card__img" src="../assets/img/500x500/02.jpg" alt="">
            </div>
            <div class="card__text">
              <h2>Titulo Do Game. </h2>
              <a href="#" class="buttons__anchor">Ir para a pagina do jogo...</a>
            </div>
          </div>
        </div>
      </section>
    </v-main>
</template>

<script lang="ts">
import { defineComponent } from 'vue';


export default defineComponent({
  name: 'LisFavView',
});
</script>

<style lang="scss" scoped>
.card-section{
  margin-left: auto;
  margin-right: auto;
  width: 80%;
  justify-items: center;
}

.card {
  display: inline-block;
  justify-items: center;
  margin-top: 5.5em;
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
      font-size: 28px;
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