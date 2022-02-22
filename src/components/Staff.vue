<template>
  <section class="bg-gray">
    <div class="container">
      <div class="row text-center">
        <div class="col-12">
          <h1 class="purple">Meet Our Staff</h1>
          <p class="text-secondary">
            With education and experience in early childhood care
          </p>
          <img src="../assets/img/header_divider.png" alt="" />
        </div>
        <div class="col-6 p-4 text-start">
          <h3>
            Our staff consists of three teachers and one assistant with
            experience in early childhood care.
          </h3>
        </div>
        <div class="col-6 p-4 text-start">
          <p>
            Praesent arcu gravida vehicula est node maecenas loareet morbi a
            dosis luctus.Urna eget lacinia eleifend praesent luctus a arcu quis
            facilisis venenatis.Aenean interdum, nibh vitae sodales,magna ante
            feugiat elit maecenas.
          </p>
        </div>
        <div
          v-for="(teacher, index) in teachers"
          :key="index"
          class="col-6 d-flex"
        >
          <div
            class="
              col-6
              p-4
              d-flex
              flex-column flex-wrap
              text-center
              justify-content-between
              align-content-end
              position-relative
            "
          >
            <img class="teacher" :src="teacher.img" alt="" />
            <h4 class="purple">{{ teacher.name }}</h4>
            <h6 class="text-secondary">{{ teacher.role }}</h6>
            <div class="quote position-absolute text-white text-end px-3 py-2">
              <img :src="require('../assets/img/quote.png')" alt="" />
            </div>
          </div>
          <div
            class="
              col-6
              d-flex
              flex-wrap
              text-start
              justify-content-center
              align-content-end
            "
          >
            <p class="text-secondary">{{ teacher.text }}</p>
            <div
              class="bg-orange text-white mx-1 my-4"
              v-for="(icon, index) in teacher.icons"
              :key="index"
            >
              <img :src="icon" />
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "Staff",
  data() {
    return {
      teachers: [
        {
          name: "Ruth Richie",
          role: "Teacher",
          text: "I have just finished my studies in Early Childhood Education,and I am also kid's yoga teacher here at Fable.I enjoy cooking,swimming and bike riding in my free time.",
          img: require("../assets/img/team_04.jpg"),
          icons: [
            require("../assets/img/mail.png"),
            require("../assets/img/facebook.png"),
            require("../assets/img/pinterest.png"),
          ],
        },
        {
          name: "Katie willmore",
          role: "Assistant Teacher",
          text: "My name is Katie.I grew up and studied in Canada.This is my second year at Fable and love every minute of it,making the children's learning experience fun",

          img: require("../assets/img/team_03.jpg"),
          icons: [
            require("../assets/img/dribbble.png"),
            require("../assets/img/stumbleupon.png"),
            require("../assets/img/instagram.png"),
          ],
        },
        {
          name: "Angelica Watson",
          role: "Lead Teacher",
          text: "I hold a degree in Early Childhood Education and an advanced English language certificate.I have been working as a kindergarten teacher since 2002.",

          img: require("../assets/img/team_02.jpg"),
          icons: [
            require("../assets/img/bing.png"),
            require("../assets/img/skype.png"),
            require("../assets/img/linkedin.png"),
          ],
        },
        {
          name: "Angela Lynn",
          role: "Teacher",
          text: "I have completed a Graduate Diploma in Early Childhood Teaching.I have worked with children aged from six weeks to eight years.This is my second year at Fable.",

          img: require("../assets/img/team_01.jpg"),
          icons: [
            require("../assets/img/youtube.png"),
            require("../assets/img/twitter.png"),
            require("../assets/img/googleplus.png"),
          ],
        },
      ],
    };
  },
};
</script>

<style scoped>
section {
  margin-top: 100px;
  padding: 100px 0 100px 0;
}
.teacher {
  max-width: 100%;
}
.quote {
  border: 2px solid #fe6601;
  top: 30%;
  left: 120%;
  transform: translate(-100%, -100%);
  width: 125px;
}
.icon {
  height: 50px;
  max-width: 50px;
}
</style>