<template>
  <section class="bg-gray">
    <div class="container">
      <div class="row text-center">
        <TitleWithDivisor :title="title" :text="text" />
        <div
          v-for="(blog, index) in news"
          :key="index"
          class="
            col-4
            d-flex
            text-start
            flex-column
            justify-content-center
            align-items-start
            py-4
          "
        >
          <h6 class="text-secondary">{{ blog.date }}</h6>
          <figure class="">
            <img :src="blog.img" alt="" />
          </figure>
          <h4 class="purple">{{ blog.title }}</h4>
          <p class="w-75 text-secondary">{{ blog.text }}</p>
          <div class="col-12 d-flex border-top py-2">
            <div class="col-6 d-flex justify-content-start align-items-center">
              <img :src="require('../assets/img/author.png')" alt="" />
              <p class="px-3 my-0">Anna Brown</p>
            </div>
            <div class="col-6 d-flex justify-content-start align-items-center">
              <img :src="require('../assets/img/category.png')" alt="" />
              <p class="px-3 my-0">Dance,Education</p>
            </div>
          </div>
        </div>
        <button class="bg-orange text-white border-0">GO TO BLOG</button>
      </div>
    </div>
  </section>
</template>

<script>
import TitleWithDivisor from "./MicroComponents/TitleWithDivisor.vue";
export default {
  name: "News",
  components: { TitleWithDivisor },
  data() {
    return {
      title: "What's New",
      text: "Fable daycare, preschool, and kindergarten",
      news: [
        {
          date: "October 03,2014",
          img: require("../assets/img/blog_09.jpg"),
          title: "Drawing and Painting Lessons",
          number: 42,
          text: "Magna est consectetur interdum modest dictum.Curabitur est faucibus, malesuada estincidunt etos et mauris,nunc a liberum govum est cuprum [...]",
        },
        {
          date: "October 03,2014",
          img: require("../assets/img/blog_10.jpg"),
          number: 19,
          title: "Fall Parents Meeting Day",
          text: "Magna est consectetur interdum modest dictum.Curabitur est faucibus, malesuada estincidunt etos et mauris,nunc a liberum govum est cuprum [...]",
        },
        {
          date: "September 20,2014",
          img: require("../assets/img/blog_08.jpg"),
          number: 22,
          title: "Birthday in Kindergarten",
          text: "Magna est consectetur interdum modest dictum.Curabitur est faucibus, malesuada estincidunt etos et mauris,nunc a liberum govum est cuprum [...]",
        },
      ],
    };
  },
};
</script>

<style scoped lang='scss'>
section {
  padding-top: 100px;
  padding-bottom: 100px;
}
figure {
  img {
    max-width: 400px;
  }
}
button {
  width: 150px;
  padding: 10px;
  margin: 0 auto;
}
</style>