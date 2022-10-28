<template>
    <section>
        <div>
            <q-carousel
                animated
                v-model="slide"
                navigation
                infinite
                :autoplay="autoplay"
                arrows
                transition-prev="slide-right"
                transition-next="slide-left"
                @mouseenter="autoplay = false"
                @mouseleave="autoplay = true"
                height="35.35rem"
                width="20rem" 
                
            >
                <q-carousel-slide :name="1" object-fit="cover"  img-src="../assets/img/19020x1080/01.jpg" />
                <q-carousel-slide :name="2" object-fit="cover" img-src="../assets/img/19020x1080/02.jpg" />
                <q-carousel-slide :name="3" object-fit="cover" img-src="../assets/img/19020x1080/03.jpg" />
            </q-carousel>
        </div>
    </section>
  </template>
  
<script lang="ts">
import { ref } from 'vue'

export default {
setup () {
    return {
    slide: ref(1),
    autoplay: ref(true)
    }
}
}
</script>

<style lang="sccs" scoped>

</style>