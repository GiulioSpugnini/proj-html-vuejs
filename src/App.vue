<template>
  <div>
    <Header :nav-items="navItems" />
    <Main />
    <Footer :footer-lists="footerLists" />
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Main from "./components/Main.vue";
import Footer from "./components/Footer.vue";

export default {
  name: "App",
  components: {
    Header,
    Main,
    Footer,
  },
  data() {
    return {
      navItems: ["Home", "Pages", "Shop", "Shortcodes", "Support", "Contact"],
      footerLists: [
        {
          title: "ABOUT US",
          text: "Elipsis magna a nulla elite forte maecenas ast elementum magna etos interdum ovum morbi vehicula morbi",
          img: require("./assets/img/logo_footer.png"),
        },
        {
          title: "ARCHIVES",
          months: [
            "OCTOBER 2014(2)",
            "SEPTEMBER 2014(2)",
            "AUGUST 2014(2)",
            "JULY 2014(2)",
            "JUNE 2014(2)",
            "MAY 2014(1)",
          ],
        },
        {
          title: "OUR FEATURES",
          text: "Nunc gravida rutrum mauris vehin hasellus ac pretium augue vivamul lacus ligul mattis ac vene:",
          lists: [
            "Friendly and welcoming place",
            "Science and art classes",
            "Positive learning environment",
            "Educational field trips",
            "Writing and reading classes",
            "Science and art classes",
          ],
        },
        {
          title: "RECENT POSTS",
          imgs: [
            {
              title: "Drawing and Painting Lessons",
              date: "October 03,2014",
              img: require("./assets/img/blog_09.jpg"),
            },
            {
              title: "Drawing and Painting Lessons",
              date: "October 03,2014",
              img: require("./assets/img/blog_10.jpg"),
            },
            {
              title: "Drawing and Painting Lessons",
              date: "October 03,2014",
              img: require("./assets/img/blog_08.jpg"),
            },
          ],
        },
      ],
    };
  },
};
</script>

<style lang="scss">
@import "./assets/scss/style.scss";
</style>
