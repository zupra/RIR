<template lang="pug">
section.Geography

  //- .BR
  h2.H География
  .MAP
    //- .num.num_bg 12
    .num.num_bg
      animated-number(
        v-observe-visibility="{callback:CB, intersection:{threshold:.7,}}"
        :value="value"
        :duration="1000"
        :delay="1000"
        :round="1"
      )

    .H_600.upper атомных городов
    div
      .pulse
      .pulse
      .pulse
      .pulse
      .pulse
      .pulse
      //-
      .pulse
      .pulse
      .pulse
      .pulse
      .pulse
      .pulse
    Slides
    img.MAP_img.img_w(
      src="~static/img/map.png"
    )
</template>

<script>
import AnimatedNumber from 'animated-number-vue'
import Slides from '~/components/Slides.vue'
export default {
  components: {
    Slides,
    AnimatedNumber
  },
  data() {
    return {
      value: 1
    }
  },
  methods: {
    CB(isVisible, entry) {
      this.value = 12
      if (!entry.isIntersecting) this.value = 1
    }
  }
}
</script>
<style lang="stylus" scoped>
// .Geography
//   opacity .4
// .MAP
//   transform translateX(50%)
</style>
