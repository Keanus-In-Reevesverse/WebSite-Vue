<template>
  <main>
    <section class="carousel-section">
      <carousel/>
    </section>
  </main>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import Carousel from '../components/Carousel.vue';


export default defineComponent({
  name: 'HomeView',
  components: {
    Carousel
},
});
</script>

<style lang="scss" scoped>
main {
  background-image: url("../assets/hero-bg.png");
  background-attachment: fixed;
  width: 100%;
  
  height: 100vh;
  
  img {
    object-fit: cover;
    height: 100%;
    width: 100%;
  }
}
.carousel-section {
  display: inline-block;
  width: 100%;
  padding-top: 6.25rem;
  
}

</style>
