<template>
  <div id="jumboFooter" class="position-absolute w-100" :style="{ backgroundImage: 'url(' + jumboFooterBg + ')' }">
          <div class="container d-flex justify-content-between">
              <h2 class="my-5 fs-1 d-inline text-light">{{title}}</h2>
              <ButtonJumbotron :textButton="textButton"/>
          </div>
      </div>
</template>

<script>
import ButtonJumbotron from './ButtonJumbotron.vue'
export default {
  components: { ButtonJumbotron },
name: 'JumboFooter',
props:['textButton', 'title'],
data(){
    return{
        jumboFooterBg: require("../../assets/img/pattern.png"),
    }
}
}
</script>

<style scoped>

</style>