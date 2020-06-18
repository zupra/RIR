<template lang="pug">
.Page
  //- WtfSvg#WtfSvg
  Intro
  .wrap.subIntro
    // Сколько вовлечено в проект
    .flex.x_sb.y_center
      InProject(
        v-prlx
      )
      WtfSvg.mt-5
    .BR
    .BR
    .BR
    //- .BR
    //- .BR

  .BG
    .wrap.SLIDE.subIntro

      Slides(
        v-prlx="{ fromBottom: true }"
      )      
      // География
      Geography(
        style="transform: scale(calc(var(--parallax-value) / 80.01 ));"
        v-prlx="{ custom: true, limit: { min: 10, max: 140 }}"
      )
      //- Возможности
      .BR
      .BR
    .wrap
      Capatibilities(
        v-prlx="{ reverse: true }"
      )
      .BR
      //- Базовые модули
      BaseModules
      .BR
      //- Дополнительные модули
      AdditionalModules
    .BR
    .BR
    //- Города-участники
    Cities
    .BR
    .wrap
      // Разработчики
      Developers
      .BR
      // Новости
      News
      .BR
    //- Форма обратной связи
      v-prlx="{ fromBottom: true }"
    Form(
    )
    // Подвал
    
    
    //- .BR
    //- .BR
    //- .BR
    Footer(
      v-prlx="{fromBottom: true, preserveInitialPosition: false}"
    )
    .BR
    .BR
</template>

<script>
import Slides from '~/components/Slides.vue'
import WtfSvg from '~/components/WtfSvg'
//
import Intro from '~/components/Intro'
import Cities from '~/components/Cities.vue'
import Form from '~/components/Form.vue'
import Footer from '~/components/Footer.vue'
import BaseModules from '~/components/BaseModules.vue'
import AdditionalModules from '~/components/AdditionalModules.vue'
import Capatibilities from '~/components/Capatibilities.vue'
import Developers from '~/components/Developers.vue'
import News from '~/components/News.vue'
import Geography from '~/components/Geography.vue'
import InProject from '~/components/InProject.vue'

export default {
  components: {
    Slides,
    WtfSvg,
    //
    Intro,
    Cities,
    Form,
    Footer,
    BaseModules,
    AdditionalModules,
    Capatibilities,
    Developers,
    News,
    Geography,
    InProject
  }
  //= ====
  /*
  data() {
    return {}
    }
  }
  */
}
</script>

<style lang="stylus">

.BG
  background #FFF

.SLIDE
  position relative

.subIntro
  line-height 1
  h2
    font-size 80px
  .num
    font-size 160px
    color: #1A3670;
    font-weight 800
  .num_bg
    background url("~static/icon/group.png") no-repeat 160px center
h2
  margin-bottom .7em
.BR
  height 4rem


body
  background: url("~static/img/ball.png") no-repeat right
  background-attachment: fixed;
  background-size: contain;
  // background-size 44vw
.Page
  //background: url("~static/img/ball.png") no-repeat right 100vh/800px;
  // background: url("~static/img/ball.png") no-repeat right 100vh/44vw
  overflow-x: hidden;
  // url("~static/img/ball_2.png")  no-repeat 90% 120vh/50vh;





.Card
  shadow()
  border-radius 5px
  background #FFF
  transition transform 0.3s
  &:hover
    transform scale(1.06) //translate(0, -6px);
    // transform: translate(0, -6px);
  ripple()


// #WtfSvg
//   position absolute
//   top calc(100vh + 40px)
//   right 30px
//   width 50vw
</style>
