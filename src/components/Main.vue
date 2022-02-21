<template>
  <main>
    <Jumbotron />
    <SliderInfo />
    <Gallery />
    <Stats/>
    <Classes/>
    <InfoList/>
    <JumboGallery/>
  </main>
</template>

<script>
import Jumbotron from "./Jumbotron.vue";
import SliderInfo from "./SliderInfo.vue";
import Gallery from "./Gallery.vue";
import Stats from "./Stats.vue";
import Classes from "./Classes.vue";
import InfoList from "./InfoList.vue";
import JumboGallery from "./JumboGallery.vue";
export default {
  name: "Main",
  components: {
    Jumbotron,
    SliderInfo,
    Gallery,
    Stats,
    Classes,
    InfoList,
    JumboGallery,

  },
};
</script>

<style>
</style>