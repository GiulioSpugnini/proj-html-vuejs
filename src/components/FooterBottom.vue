<template>
  <section class="bg-white text-center">
    <div class="container d-flex justify-content-center align-items-center">
      <div
        class="bg-orange text-white mx-1 my-4"
        v-for="(icon, index) in icons"
        :key="index"
      >
        <img :src="icon" alt="" />
      </div>
    </div>
    <p class="text-secondary">
      Fable - Children kindergarten WordPress Theme by QuanticaLabs
    </p>
  </section>
</template>

<script>
export default {
  name: "FooterBottom",
  data() {
    return {
      icons: [
        require("../assets/img/behance.png"),
        require("../assets/img/dribbble.png"),
        require("../assets/img/envato.png"),
        require("../assets/img/facebook.png"),
        require("../assets/img/twitter.png"),
      ],
    };
  },
};
</script>

<style scoped>
section {
  min-height: 100px;
}
</style>