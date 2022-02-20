<template>
  <main>
    <Jumbotron />
    <SliderInfo />
    <Gallery />
  </main>
</template>

<script>
import Jumbotron from "./Jumbotron.vue";
import SliderInfo from "./SliderInfo.vue";
import Gallery from "./Gallery.vue";
export default {
  name: "Main",
  components: {
    Jumbotron,
    SliderInfo,
    Gallery,
  },
};
</script>

<style>
</style>