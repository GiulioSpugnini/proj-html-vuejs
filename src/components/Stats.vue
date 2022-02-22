<template>
  <section :style="{ backgroundImage: 'url(' + statsBg + ')' }">
    <div class="container h-100">
      <div class="row h-100 justify-content-center align-items-center text-white">
        <div class="col-3 text-center">
          <div class="rounded-circle circle">
            <h2 class="">507</h2>
          </div>
          <h4>Our Pupils</h4>
          <p>Pulvinar forte maestro node terminal est elipsis prism.</p>
        </div>
        <div class="col-3 text-center">
          <div class="rounded-circle circle">
            <h2 class="">235</h2>
          </div>
          <h4>Teaching Hours</h4>
          <p>Elipsis morbi nulla a metro interdum vitae elite.</p>
        </div>
        <div class="col-3 text-center">
          <div class="rounded-circle circle">
            <h2 class="">100%</h2>
          </div>
          <h4>Satisfied Parents</h4>
          <p>Elementum pulvinar detos diaspis movum blandit.</p>
        </div>
        <div class="col-3 text-center">
          <div class="rounded-circle circle">
            <h2 class="">1050</h2>
          </div>
          <h4>Meals Per Year</h4>
          <p>Pulvinar forte maestro node terminal est elipsis prism.</p>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "Stats",
  data() {
    return {
      statsBg: require("../assets/img/parallax_01.jpg"),
    };
  },
};
</script>

<style scoped lang="scss">
section {
  height: 450px;
  background-position: center;
}
.circle {
  border: 1px solid white;
  width: 150px;
  height: 150px;
  padding-top: 50px;
  margin: 0 auto;
}
h4{
    margin-top: 20px;
    margin-bottom: 20px;
}
</style>