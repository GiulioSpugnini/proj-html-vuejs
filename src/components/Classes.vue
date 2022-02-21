<template>
  <section class="container">
    <div class="row text-center">
      <div class="col-12">
        <h1>Our Classes</h1>
        <p class="text-secondary">
          Our preschool program has four dedicated classes
        </p>
        <img src="../assets/img/header_divider.png" alt="" />
      </div>
      <div
        v-for="(classe, index) in classes"
        :key="index"
        class="col-6 d-flex align-items-center gy-4"
      >
        <div
          class="
            col-6
            d-flex
            flex-column
            justify-content-between
            bg-purple
            h-100
            text-white
          "
        >
          <div class="col-8 p-3 text-start">
            <h3>{{ classe.title }}</h3>
            <p class="lightgray fw-bolder">Class name</p>
          </div>
          <div class="col-4 d-flex w-100">
            <div class="col-6 py-2 border-classe">
              <h6>{{ classe.age }}</h6>
              <h6 class="lightgray">{{ classe.year }}</h6>
            </div>
            <div class="col-6 py-2">
              <h6>{{ classe.classSize }}</h6>
              <h6 class="lightgray">Class size</h6>
            </div>
          </div>
        </div>
        <div class="col-6 position-relative">
          <img class="classe" :src="classe.img" alt="" />
          <button class="position-absolute bg-orange text-white border-0 p-2">READ MORE</button>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "Classes",
  data() {
    return {
      classes: [
        {
          title: "Little Lambs",
          age: "12-24",
          year: "Month olds",
          classSize: 9,
          img: require("../assets/img/class_01-690x506.jpg"),
        },
        {
          title: "Bouncy Bears",
          age: "2-3",
          year: "Years olds",
          classSize: 12,
          img: require("../assets/img/class_02-690x506.jpg"),
        },
        {
          title: "Tenderhearts",
          age: "3-4",
          year: "Years olds",
          classSize: 15,
          img: require("../assets/img/class_03-690x506.jpg"),
        },
        {
          title: "Shining Stars",
          age: "4-5",
          year: "Years olds",
          classSize: 20,
          img: require("../assets/img/class_04-690x506.jpg"),
        },
      ],
    };
  },
};
</script>

<style scoped>
section{
  padding: 100px 0 100px 0;
}
.classe {
  max-width: 100%;
}
.border-classe {
  border-right: 1px solid gray;
  height: 60px;
}
button{
  top: 100%;
  transform: translate(-100%, -100%);
  width: 150px;
}
</style>