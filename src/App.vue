<template>
  <div class="app">
    <v-header>
      <navigation/>
    </v-header>
    <v-main>
      <router-view/>
    </v-main>
    <v-footer>
      <skirting/>
    </v-footer>
  </div>
</template>


<script setup lang="ts">
import { RouterView } from 'vue-router'
import Navigation from './components/Navigation.vue';
import Skirting from './components/Skirting.vue';


</script>

<style lang="scss" scoped>
.app {
  min-height: 100vh;
  position: relative;
  background-image: url("./assets/hero-bg.png");
}

</style>
