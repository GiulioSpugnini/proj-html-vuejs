<template>
  <section>
    <div class="position-relative jumbo">
      <img v-for="(img, index) in imgs" :key="index" :src="img" alt="" />
      <div
        id="jumboFooter"
        class="position-absolute w-100"
        :style="{ backgroundImage: 'url(' + jumboFooterBg + ')' }"
      >
        <div class="container d-flex justify-content-between">
          <h2 class="my-5 fs-1 d-inline text-light">
            See Our Kindergarten Photo Gallery!
          </h2>
          <button class="px-3 m-5 bg-transparent text-white">VIEW GALLERY</button>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "JumboGallery",
  data() {
    return {
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
button:hover{
 background-color: white !important;
 color: #4c4a9b !important;
}
</style>