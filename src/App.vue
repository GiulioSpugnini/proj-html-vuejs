<template>
  <div>
    <Header :navItems='navItems' />
    <Main />
    <Footer />
  </div>
</template>

<script>
import Header from './components/Header.vue';
import Main from './components/Main.vue';
import Footer from './components/Footer.vue';

export default {
  name: 'App',
  components: {
    Header,
    Main,
    Footer,
  },
  data(){
    return{
      navItems: ['Home','Pages','Shop','Shortcodes','Support','Contact'],
    }
  }
}
</script>

<style lang="scss">
@import "./assets/scss/style.scss";
</style>
