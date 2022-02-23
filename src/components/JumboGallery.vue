<template>
  <section>
    <div class="position-relative jumbo">
      <img v-for="(img, index) in imgs" :key="index" :src="img" alt="" />
      <div
        id="jumboFooter"
        class="position-absolute w-100"
        :style="{ backgroundImage: 'url(' + jumboFooterBg + ')' }"
      >
        <JumboFooter :textButton="textButton" :title="title"/>
      </div>
    </div>
  </section>
</template>

<script>
import JumboFooter from './MicroComponents/JumboFooter.vue';
export default {
  components: { JumboFooter },
  name: "JumboGallery",
  data() {
    return {
      title: 'See Our Kindergarten Photo Gallery!',
      textButton: 'VIEW GALLERY',
      jumboBg: require("../assets/img/slider_slide3_background.png"),
      jumboFooterBg: require("../assets/img/pattern.png"),
      imgs: [
        require("../assets/img/gallery_01.jpg"),
        require("../assets/img/gallery_02.jpg"),
        require("../assets/img/gallery_03.jpg"),
        require("../assets/img/gallery_04.jpg"),
      ],
    };
  },
};
</script>

<style scoped>
.jumbo {
  min-height: 300px;
}
img {
  width: calc(100% / 4);
}
#car {
  top: 70%;
  left: 70%;
}
#breaks {
  top: 60%;
  left: 40%;
}
#jumboFooter {
  top: 100%;
  left: 0;
}
</style>