<template>
  <div class="home">
    <section class="hero">

    </section>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';


export default defineComponent({
  name: 'HomeView',
  components: {
},
});
</script>

<style lang="scss" scoped>
.hero {
  background-image: url("../assets/hero-bg.png");
  background-attachment: fixed;
  position: relative;
  height: 100vh;
  img {
    object-fit: cover;
    height: 100%;
    width: 100%;
  }
}
</style>
