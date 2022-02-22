<template>
  <section class="bg-gray text-center align-self-end">
    <div class="container d-flex justify-content-center align-items-center">
      <div
        class="bg-orange text-white mx-1 my-4"
        v-for="(icon, index) in icons"
        :key="index"
      >
        <img :src="icon" alt="" />
      </div>
    </div>
    <p class="text-secondary m-0">
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
  margin-top: 100px;
  min-height: 100px;
}
</style>