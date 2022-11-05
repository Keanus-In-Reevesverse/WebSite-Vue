<template>
    <v-main>

    </v-main>
</template>

<script lang="ts">

</script>

<script lang="scss">
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
</script>