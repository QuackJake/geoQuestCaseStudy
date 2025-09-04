<script setup>
import 'vue3-carousel/carousel.css'
import { Carousel, Slide, Navigation } from 'vue3-carousel'

defineProps({
  images: {
    type: Array,
    required: true
  },
  header: {
    type: String,
    required: true
  }
});

const config = {
  height: 750,
  itemsToShow: 3,
  gap: 4,
  autoplay: 4000,
  wrapAround: true,
  pauseAutoplayOnHover: true,
}
</script>

<template>
  <div class="p-12" style="background: linear-gradient(to right, #D0F3FD, #8183DD);">
    <section class="w-[75vw] mx-auto">
      <h2 class="text-4xl md:text-4xl font-bold text-primary mb-12 text-center leading-snug">
        {{ header }}
      </h2>
      <Carousel v-bind="config">
        <Slide v-for="image in images" :key="image.id">
          <img :src="image.url" alt="image" />
        </Slide>
        <template #addons>
          <Navigation />
        </template>
      </Carousel>
    </section>
  </div>
</template>

<style>
:root {
  background-color: #242424;
}

.carousel {
  --vc-nav-background: rgba(255, 255, 255, 0.7);
  --vc-nav-border-radius: 100%;
}

img {
  border-radius: 8px;
  width: auto;
  height: 100%;
  max-height: 700px; /* Optional: limit max height */
  display: block;
  margin: 0 auto;
  object-fit: contain; /* keeps portrait ratio without stretching */
}
</style>
