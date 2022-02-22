<template>
  <main>
    <Jumbotron />
    <SliderInfo />
    <Gallery />
    <Stats/>
    <Classes/>
    <InfoList/>
    <JumboGallery/>
    <Staff/>
    <Quotes/>
    <News/>
    <Maps/>
    <Contacts/>
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
import Staff from "./Staff.vue";
import Quotes from "./Quotes.vue";
import News from "./News.vue";
import Maps from "./Maps.vue";
import Contacts from "./Contacts.vue";
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
    Staff,
    Quotes,
    News,
    Maps,
    Contacts,

  },
};
</script>

<style>
</style>