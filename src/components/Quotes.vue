<template>
  <section :style="{ backgroundImage: 'url(' + quotesBg + ')' }">
    <div class="container h-100">
      <div
        class="
          row
          h-100
          justify-content-center
          align-items-center
          text-center text-white
        "
      >
        <div class="col-12 circle">
          <img :src="require('../assets/img/quote_alt.png')" alt="" />
        </div>
        <div class="col-12">
          <h1>
            Fable Kindergarten is a great place for my daughter to start her
            schooling experience.It's welcoming and safe and my daugher love
            being here.
          </h1>
          <div class="divisor py-2"></div>
          <h6 class="py-3">Joe R.Hamblen</h6>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "Quotes",
  data() {
    return {
      quotesBg: require("../assets/img/parallax_02.jpg"),
    };
  },
};
</script>

<style scoped lang="scss">
section {
  padding-top: 100px;
  padding-bottom: 100px;
  background-position: center;
}
.divisor {
  border-bottom: 1px solid white;
  max-width: 50px;
  margin: 0 auto;
}
.circle {
  border: 2px solid white;
  border-radius: 50%;
  width: 80px;
  height: 80px;
  line-height: 70px;
  margin: 0 auto;
}
h4 {
  margin-top: 20px;
  margin-bottom: 20px;
}
</style>