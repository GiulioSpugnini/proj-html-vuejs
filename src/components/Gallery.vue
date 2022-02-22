<template>
  <section class="bg-gray">
    <div class="container d-flex">
      <div class="col-6 d-flex flex-column justify-content-between">
        <div>
          <button class="p-3 text-secondary border-0">Overview</button>
          <button class="p-3 text-secondary border-0 mx-4">Our Mission</button>
        </div>
        <div>
          <h3 class="w-75 purple">
            Our philosophy is learning through play as we offer a stimulating
            environment for children.
          </h3>
        </div>
        <div class="d-flex">
          <div
            id="clock"
            class="bg-orange rounded-circle text-center flex-shrink-0"
          >
            <img src="../assets/img/clock_alt.png" alt="" />
          </div>
          <div>
            <h4 class="mx-4 purple">Full Day Sessions</h4>
            <p class="w-75 mx-4 text-secondary">
              Pulvinar est metro ligula blandit maecenas retrum gravida
              cuprum.Maecenas node estibulum.
            </p>
          </div>
        </div>
        <div class="d-flex">
          <div
            id="linked"
            class="bg-orange rounded-circle text-center flex-shrink-0"
          >
            <img src="../assets/img/diagram_alt.png" alt="" />
          </div>
          <div>
            <h4 class="mx-4 purple">Full Day Sessions</h4>
            <p class="w-75 mx-4 text-secondary">
              Pulvinar est metro ligula blandit maecenas retrum gravida
              cuprum.Maecenas node estibulum.
            </p>
          </div>
        </div>
      </div>
      <div class="col-6 text-center">
        <div class="d-flex justify-content-center">
          <figure v-for="(image, index) in 1" :key="index" id="selectedImg">
            <img :src="images[currentIndex]" />
          </figure>
        </div>
        <div class="d-flex justify-content-center">
          <figure v-for="(image, index) in images" :key="index">
            <img class="imgs" role="button" @click="isActive(index)" :src="image" />
          </figure>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "Gallery",
  data() {
    return {
      currentIndex: 0,
      images: [
        require("../assets/img/gallery_07-690x506.jpg"),
        require("../assets/img/gallery_01-690x506.jpg"),
        require("../assets/img/gallery_08-690x506.jpg"),
      ],
    };
  },
  methods: {
    isActive(index) {
      return this.currentIndex=index ;
    },
  },
};
</script>

<style scoped lang='scss'>
section {
  padding: 100px 0 100px 0;
}
figure {
  .imgs:nth-child(1) {
    width: 136px;
    margin-right: 10px;
    margin-left: 10px;
  }
}
#clock,
#linked {
  width: 100px;
  height: 100px;
  line-height: 90px;
}
#selectedImg img {
  max-width: 450px;
}
img{
  border: 2px solid transparent;
}
img:hover{
  border-bottom: 2px solid #fe6601;
}
button:hover{
  background-color: #fe6601 !important;
  color: white !important;
}
</style>