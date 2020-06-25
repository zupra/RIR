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
      .pulse(
        v-for="(name, idx) of ['Глазов', 'Новоуральск', 'Саров', 'Железногорск', 'Заречный', 'Заречный', 'Лесной', 'Озёрск', 'Северск', 'Снежинск', 'Трёхгорный', 'Зеленогорск']"
        :key="idx"
        :title="name"
        :class="{curr_pulse: idx === pulse}"
      )
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
  props: {
    pulse: {
      type: Number,
      default: 0
    }
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
<style lang="stylus">




.curr_pulse
  background $blue_l
  z-index 10
  box-shadow: 0 0 0 10px rgba($blue_l, .1);
  // transform scale(3) !important
  // transition: transform 0.4s;
  // transform scale(1.1) !important
  // animation none
  animation: scale 5s;

  &:after
    position absolute
    top 13px
    left 6px
    font-size 4px
    content: attr(title)
    color #222
    transform translateX(-50%)


@keyframes scale

  0%
    transform scale(1)

  25%
    transform scale(3)

  75%
    transform scale(3)

  100%
    transform scale(1)

// .Geography
//   opacity .4
// .MAP
//   transform translateX(50%)
</style>
