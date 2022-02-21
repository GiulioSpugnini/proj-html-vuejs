<template>
  <footer class="position-relative bg-purple">
    <div class="container">
      <div class="row">
        <div
          v-for="(footerList, index) in footerLists"
          :key="index"
          class="col-3"
        >
          <ul class="text-start text-light">
            <li class="my-4">
              {{ footerList.title }}
              <div class="divisor"></div>
            </li>
            <li class="my-3">{{ footerList.text }}</li>
            <li class="my-4" v-if="index == 0"><img :src="footerList.img" alt="" /></li>
            <li
              class="border p-2 m-1 list-"
              v-for="(month, index) in footerList.months"
              :key="index"
            >
              {{ month }}
            </li>
            <li v-for="(list, index) in footerList.lists" :key="index">
              <img
                class="icon"
                :src="require('../assets/img/style_4_alt.png')"
                alt=""
              />{{ list }}
            </li>
            <li v-for="(post, index) in footerList.imgs" :key="index">
              <div class="col-4 w-50">
                <div class="row flex-nowrap w-100">
                  <div class="col-6 w-100"><img :src="post.img" alt="" /></div>
                  <div class="col-6 d-flex flex-wrap w-100">
                    <h6 class="">{{ post.title }}</h6>
                    <img class="icon" :src="require('../assets/img/date_footer.png')" alt="">
                    <p>{{post.date}}</p>
                  </div>
                </div>
              </div>
            </li>
          </ul>
        </div>
      </div>
    </div>
    <FooterBottom/>
  </footer>
</template>

<script>
import FooterBottom from "./FooterBottom.vue";
export default {
  name: "Footer",
  props: ["footerLists"],
  components:{FooterBottom},
};
</script>

<style lang="scss" scoped>
footer {
  margin-top: 180px;
  .divisor {
    border-bottom: 2px solid slategray;
    max-width: 50px;
  }
}
img {
  max-width: 200px;
  height: 60px;
}
.icon {
  max-width: 15px;
  max-height: 15px;
  margin-right: 10px;
}
h6{
  font-size: 14px;
}
p{
  font-size: 12px;
}
</style>

