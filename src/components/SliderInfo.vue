<template>
  <section class="container">
    <div class="row text-center">
      <TitleWithDivisor :title="title" :text="text" />
      <div class="col-3 d-flex flex-column align-items-center">
        <figure class="bg-orange">
          <img src="../assets/img/schoolbag_alt.png" alt="" />
        </figure>
        <h4 class="purple">Morbi Etos</h4>
        <p>
          Praesent interdum est gravida vehicula est node maecenas loareet morbi
          a dosis luctus novum est praesent.
        </p>
      </div>
      <div class="col-3 d-flex flex-column align-items-center">
        <figure class="bg-purple">
          <img src="../assets/img/stroller_alt.png" alt="" />
        </figure>
        <h4 class="purple">Congue Gravida</h4>
        <p>
          Elipsis magna a terminal nulla elementum morbi elite forte maecenas
          sest magna etos interdum vitae est.
        </p>
      </div>
      <div class="col-3 d-flex flex-column align-items-center">
        <figure class="bg-orange">
          <img src="../assets/img/globe_alt.png" alt="" />
        </figure>
        <h4 class="purple">Maecenas Node</h4>
        <p>
          Praesent interdum est gravida vehicula est node maecenas loareet morbi
          a dosis luctus novum est praesent.
        </p>
      </div>
      <div class="col-3 d-flex flex-column align-items-center">
        <figure class="bg-purple">
          <img src="../assets/img/bell_alt.png" alt="" />
        </figure>
        <h4 class="purple">Praesent Morbi</h4>
        <p>
          Elipsis magna a terminal nulla elementum morbi elite forte maecenas
          sest magna etos interdum vitae est.
        </p>
      </div>
    </div>
  </section>
</template>

<script>
import TitleWithDivisor from "./MicroComponents/TitleWithDivisor.vue";
export default {
  name: "Slider-info",
  components: { TitleWithDivisor },
  data() {
    return {
      title: "Welcome to Fable",
      text: "Fable daycare, preschool, and kindergarten",
    };
  },
};
</script>

<style scoped lang='scss'>
section {
  margin-top: 200px;
  margin-bottom: 100px;
}
figure {
  max-width: 200px;
  max-height: 200px;
  border-radius: 50%;
  padding: 50px;
}
</style>