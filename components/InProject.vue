<template lang="pug">
section#About

  .BR
  h2.H В проекте
    br
    | участвуют

  WtfSvg#WtfSvg

  //- .num 880
  animated-number.num(
    v-observe-visibility="{callback:CB_1, intersection:{threshold:0.7,}}"
    :value="val_1"
    :duration="3000"
    :round="1"
  )
  .H_600.upper тысяч жителей вовлечены
    br
    | в улучшение городской среды

  .my-5
    //- .num.num_bg 12
    .num.num_bg
      animated-number(
        v-observe-visibility="{callback:CB_2, intersection:{threshold:0.7,}}"
        :value="val_2"
        :duration="1000"
        :delay="1000"
        :round="1"
      )
    .H_600.upper атомградов используют
      br
      | умные цифровые сервисы
  .BR
</template>

<script>
import AnimatedNumber from 'animated-number-vue'
import WtfSvg from '~/components/WtfSvg'
export default {
  components: {
    WtfSvg,
    AnimatedNumber
  },
  data() {
    return {
      val_1: 1,
      val_2: 1
    }
  },
  methods: {
    CB_1(isVisible, entry) {
      this.val_1 = 880
      // console.log(this.isVisible)
      // console.info('entry', entry)
      if (!entry.isIntersecting) this.val_1 = 1
    },
    CB_2(isVisible, entry) {
      this.val_2 = 12
      if (!entry.isIntersecting) this.val_2 = 1
    }
  }
}
</script>

<style lang="stylus" scoped>
#About
  position relative


#WtfSvg
  position absolute
  top 5em
  right -10vw
  width 40vw
</style>
