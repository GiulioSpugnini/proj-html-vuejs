<template>
  <header class="container d-flex justify-content-between align-items-center">
    <div class="col-4">
      <img src="../assets/img/logo.png" alt="" />
    </div>
    <div class="col-8">
      <ul class="d-flex justify-content-evenly">
        <li v-for="(navItem, index) in navItems" :key="index">
          <figure class="text-center">
            <img class="nav-icons" :src=" require(`../assets/img/${navItem.toLowerCase()}.png`) " alt="">
            <figcaption>{{ navItem }}</figcaption>
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
.nav-icons{
  
}
</style>
