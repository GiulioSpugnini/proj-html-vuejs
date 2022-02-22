<template>
  <section :style="{ backgroundImage: 'url(' + jumboBg + ')' }">
    <div class="position-relative jumbo">
      <img id="car" class="position-absolute" src="../assets/img/slider_slide3_img3.png" />
      <img id="breaks" class="position-absolute" src="../assets/img/slider_slide3_img2.png" />
      <img id="twoFemale" class="position-absolute" src="../assets/img/slider_slide3_img1.png" />
      <img id="baby" class="position-absolute" src="../assets/img/slider_slide1_img1.png" />
      <img id="babyAbaco" class="position-absolute" src="../assets/img/slider_slide1_img2.png" />
      <div id="jumboFooter" class="position-absolute w-100" :style="{ backgroundImage: 'url(' + jumboFooterBg + ')' }">
          <div class="container d-flex justify-content-between">
              <h2 class="my-5 fs-1 d-inline text-light">How to Enroll Your Child to a Class?</h2>
              <button class="px-3 m-5 bg-transparent text-white">LEARN MORE</button>
          </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "jumbotron",
  data() {
    return {
      autoplay: undefined,
      jumboBg: require("../assets/img/slider_slide3_background.png"),
      jumboFooterBg: require("../assets/img/pattern.png"),
    };
  },
  methods:{
    nextImg() {
            this.currentIndex = (this.currentIndex === this.images.length - 1) ? 0 : (this.currentIndex + 1);
        },
        prevImg() {
            this.currentIndex = (this.currentIndex === 0) ? (this.images.length - 1) : (this.currentIndex - 1);
        },
    startAutoplay() {
            this.autoplay = setInterval(this.nextImg, 3000)
        },
        stopAutoplay() {
            clearInterval(this.autoplay);
        },
  },
  created() {
        this.startAutoplay();
    }
};
</script>

<style>
.jumbo {
  min-height: 600px;
}
#car{
 top: 70%;
 left: 70%;
 z-index: 1;
}
#breaks{
    top: 60%;
 left: 40%;
 z-index: 1;
}
#jumboFooter{
    top: 100%;
    left: 0;
    
}
#twoFemale{
top: 10%;
  left: 50%;
}
#baby{
top: 0%;
  left: 5%;
}
#babyAbaco{
  top: 0%;
  left: 55%;
}
button{
  border: 2px solid white;
}
</style>