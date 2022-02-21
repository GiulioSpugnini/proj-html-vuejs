<template>
  <section class="bg-gray">
      <div class="container d-flex">
          <div class="col-6 d-flex flex-column justify-content-between w-50">
              <div class="col-4 purple w-100">
                  <h3 class="w-100">
                  We have been educating children for over fifteen years.Our goeal is to create a place that engages each child.</h3>
                  </div>
              <div class="col-4 text-secondary w-100">
                  <p class="w-100">Praesent arcu gravida vehicula est node maecenas loareet morbi a dosis luctus.Urna eget lacinia eleifend praesent luctus a arcu quis facilisis venenatis aenean interdum.</p>
              </div>
              <div class="col-4 w-100">
                  <ul>
                      <li class="text-secondary" v-for="(list,index) in lists" :key="index"><img src="../assets/img/style_1.png" alt="">{{list}}</li>
                      
                  </ul>
              </div>
          </div>
          <div class="col-6 d-flex flex-wrap w-50 text-center">
              <div v-for="(info,index) in infos" :key="index" class="col-6 d-flex flex-column align-items-center">
                  <figure class="rounded-circle w-25 d-inline p-4 bg-light"><img :src="info.icon" alt=""></figure>
                  <h5 class="m-2 purple">{{info.title}}</h5>
                  <p class="m-2 text-secondary m-0">{{info.text}}</p>
              </div>
          </div>
      </div>
  </section>
</template>

<script>
export default {
name: 'InfoList',
data(){
    return{
        lists:['Comprehensive reporting on individual achievment','Educational field trips and school presentations','Individual attention in a small-class setting','Learning program with after-school care','Opportunities to carry out scientific investigations','Positive learning environment for your child'],
        infos:[
            {
                icon: require('../assets/img/toy.png'),
                title: 'Learning & Fun',
                text: 'Praesent modea est gravida node vehicula luctus.'
        },
            {
                icon: require('../assets/img/meal.png'),
                title: 'Learning & Fun',
                text: 'Praesent modea est gravida node vehicula luctus.'
        },
            {
                icon: require('../assets/img/school.png'),
                title: 'Learning & Fun',
                text: 'Praesent modea est gravida node vehicula luctus.'
        },
            {
                icon: require('../assets/img/shield.png'),
                title: 'Learning & Fun',
                text: 'Praesent modea est gravida node vehicula luctus.'
        },
        ],
        
    }
}
}
</script>

<style scoped lang="scss">
section{
    padding-top: 100px;
    padding-bottom: 100px;
}
ul{
    padding: 0;
    li{
        list-style-type: none;
        img{
            margin-right: 10px;
        }
    }
}
</style>