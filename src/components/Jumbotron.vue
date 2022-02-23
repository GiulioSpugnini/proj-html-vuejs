<template>
  <section :style="{ backgroundImage: 'url(' + jumboBg + ')' }">
    <div class="position-relative jumbo">
      <img
        id="car"
        class="position-absolute"
        src="../assets/img/slider_slide3_img3.png"
      />
      <img
        id="breaks"
        class="position-absolute"
        src="../assets/img/slider_slide3_img2.png"
      />
      <div v-for="(baby, index) in babies" :key="index">
        <img
          v-if="index === currentIndex"
          class="position-absolute fade-in-image"
          :style="{ top: baby.top } && { left: baby.left }"
          :src="baby.img"
        />
      </div>
      <JumboFooter :textButton="textButton" :title="title" />
    </div>
  </section>
</template>

<script>
import JumboFooter from "./MicroComponents/JumboFooter.vue";
export default {
  components: { JumboFooter },
  name: "jumbotron",
  data() {
    return {
      title: "How to Enroll Your Child to a Class?",
      textButton: "LEARN MORE",
      currentIndex: 0,
      autoplay: undefined,
      babies: [
        {
          img: require("../assets/img/slider_slide3_img1.png"),
          top: "10%",
          left: "50%",
        },
        {
          img: require("../assets/img/slider_slide1_img1.png"),
          top: "0%",
          left: "5%",
        },
        {
          img: require("../assets/img/slider_slide1_img2.png"),
          top: "0%",
          left: "55%",
        },
      ],
      jumboBg: require("../assets/img/slider_slide3_background.png"),
    };
  },
  methods: {
    isActive(index) {
      return index == this.currentIndex;
    },
    nextImg() {
      this.currentIndex = this.currentIndex === 2 ? 0 : this.currentIndex + 1;
    },
    startAutoplay() {
      this.autoplay = setInterval(this.nextImg, 3000);
    },
    stopAutoplay() {
      clearInterval(this.autoplay);
    },
  },
  created() {
    this.startAutoplay();
  },
};
</script>

<style>
.fade-in-image {
  animation: fadeIn 3s;
}
@keyframes fadeIn {
  0% {
    opacity: 0;
  }
  50% {
    opacity: 1;
  }
  100% {
    opacity: 0;
  }
}
.jumbo {
  min-height: 600px;
}
#car {
  top: 70%;
  left: 70%;
  z-index: 1;
}
#breaks {
  top: 60%;
  left: 40%;
  z-index: 1;
}
#jumboFooter {
  top: 100%;
  left: 0;
}
#twoFemale {
  top: 15%;
  left: 50%;
}
#baby {
  top: 0%;
  left: 5%;
}
#babyAbaco {
  top: 0%;
  left: 55%;
}
</style>