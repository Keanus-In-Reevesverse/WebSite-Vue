<template>
  <div class="app">
    <header>
      <navigation/>
    </header>
    <main>
      <router-view/>
    </main>
    <footer>
      <skirting/>
    </footer>
  </div>
</template>


<script setup lang="ts">
import { RouterView } from 'vue-router'
import Navigation from './components/Navigation.vue';
import Skirting from './components/Skirting.vue';


</script>

<style lang="scss" scoped>
.app {
  background-image: url("./assets/hero-bg.png");
  min-height: 100vh;
  position: relative;
  background-color: #f1f1f1;
}

</style>
