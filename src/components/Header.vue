<template>
  <header class="container d-flex justify-content-between align-items-center">
    <div class="col-4 text-center">
      <img src="../assets/img/logo.png" alt="" />
    </div>
    <div class="col-8">
      <ul class="d-flex justify-content-evenly align-items-center m-0 p-0">
        <li v-for="(navItem, index) in navItems" :key="index">
          <figure class="text-center">
            <img :src=" require(`../assets/img/${navItem.toLowerCase()}.png`) " alt="">
            <figcaption class="fs-5 my-3">{{ navItem }}</figcaption>
          </figure>
        </li>
      </ul>
    </div>
  </header>
</template>

<script>
export default {
  name: "Header",
  props: ["navItems"],
};
</script>

<style scoped lang="scss">
@import '../assets/scss/style.scss';
figcaption{
  color: $navbar-color;
}
li:hover{
  background-color: #fe6601;
}
</style>
