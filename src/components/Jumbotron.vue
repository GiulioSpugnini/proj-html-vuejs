<template>
  <section :style="{ backgroundImage: 'url(' + jumboBg + ')' }">
    <div class="position-relative jumbo">
      <img id="car" class="position-absolute" src="../assets/img/slider_slide3_img3.png" alt="" />
      <img id="breaks" class="position-absolute" src="../assets/img/slider_slide3_img2.png" alt="" />
      <div id="jumboFooter" class="position-absolute w-100" :style="{ backgroundImage: 'url(' + jumboFooterBg + ')' }">
          <div class="container d-flex justify-content-between">
              <h2 class="my-5 fs-1 d-inline text-light">How to Enroll Your Child to a Class?</h2>
              <button class="px-3 m-5">LEARN MORE</button>
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
      jumboBg: require("../assets/img/slider_slide3_background.png"),
      jumboFooterBg: require("../assets/img/pattern.png"),
    };
  },
};
</script>

<style>
.jumbo {
  min-height: 600px;
}
#car{
 top: 70%;
 left: 70%;
}
#breaks{
    top: 60%;
 left: 40%;
}
#jumboFooter{
    top: 100%;
    left: 0;
}
</style>