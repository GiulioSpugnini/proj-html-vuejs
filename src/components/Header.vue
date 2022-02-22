<template>
  <header class="container d-flex justify-content-between">
    <div class="col-4 text-center">
      <img src="../assets/img/logo.png" alt="" />
    </div>
    <div class="col-8">
      <ul class="col-12 h-100 d-flex justify-content-evenly align-items-center m-0 p-0">
        <li class="col-2 h-100" v-for="(navItem, index) in navItems" :key="index">
          <section class="text-center m-0">
            <img :src=" require(`../assets/img/${navItem.toLowerCase()}.png`) " alt="">
            <h5 class="purple">{{ navItem }}</h5>
          </section>
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
section{
  line-height: 80px;
}
ul{
  cursor: pointer;
}
li:hover{
  background-color: #fe6601;
  color: white;
}
</style>
