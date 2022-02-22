<template>
  <section :style="{ backgroundImage: 'url(' + jumboBg + ')' }">
    <div class="position-relative jumbo">
      <img id="car" class="position-absolute" src="../assets/img/slider_slide3_img3.png" />
      <img id="breaks" class="position-absolute" src="../assets/img/slider_slide3_img2.png" />
      <div v-for="(baby,index) in babies" :key="index">
      <img v-if="index===currentIndex" class="position-absolute" :style="{top: baby.top}&& {left: baby.left}" :src="baby.img" />

      </div>
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
      currentIndex: 0,
      autoplay: undefined,
      babies:[
        {
          img: require("../assets/img/slider_slide3_img1.png"),
          top: '10%',
          left: '50%',
         
        },
        {
          img: require("../assets/img/slider_slide1_img1.png"),
          top: '0%',
          left: '5%',
          
        },
        {
          img: require("../assets/img/slider_slide1_img2.png"),
          top: '0%',
          left: '55%',
         
        },
      ],
      jumboBg: require("../assets/img/slider_slide3_background.png"),
      jumboFooterBg: require("../assets/img/pattern.png"),
    };
  },
  methods:{
     isActive(index) {
            return index == this.currentIndex;
        },
    nextImg() {
            this.currentIndex = (this.currentIndex === 2) ? 0 : (this.currentIndex + 1);
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