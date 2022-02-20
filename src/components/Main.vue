<template>
  <main>
    <Jumbotron />
    <SliderInfo />
    <Gallery />
    <Stats/>
  </main>
</template>

<script>
import Jumbotron from "./Jumbotron.vue";
import SliderInfo from "./SliderInfo.vue";
import Gallery from "./Gallery.vue";
import Stats from "./Stats.vue";
export default {
  name: "Main",
  components: {
    Jumbotron,
    SliderInfo,
    Gallery,
    Stats,
  },
};
</script>

<style>
</style>