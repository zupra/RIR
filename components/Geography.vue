<template lang="pug">
section
  h2.H География
  .MAP
    div.flex.y_center
      .num 12
      .city_logo_container.flex.flex_wr
        img(

          class="city_logo_item"
          v-for="_,idx in Array(12)"
          :src="require(`~/static/icon/logo_of_сities/${idx + 1}.png`)"
        )
    .text_x3 АТОМНЫХ ГОРОДОВ
    div
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
import Slides from '~/components/Slides.vue'
export default {
  name: 'Geography',
  components: {
    Slides
  }
}
</script>
<style lang="stylus" scoped>
.city_logo_container
  max-width 203px
  margin-left 41px
  position relative
.city_logo_item
  margin-bottom 12px
  width 58px
  height 58px
  &:not(first-child)
    margin-left -28px
.city_logo_item:nth-child(1)
  z-index 13
.city_logo_item:nth-child(2)
  z-index 12
.city_logo_item:nth-child(3)
  z-index 11
.city_logo_item:nth-child(4)
  z-index 10
.city_logo_item:nth-child(5)
  z-index 9
.city_logo_item:nth-child(6)
  z-index 8
.city_logo_item:nth-child(7)
  z-index 7
.city_logo_item:nth-child(8)
  z-index 6
.city_logo_item:nth-child(9)
  z-index 5
.city_logo_item:nth-child(10)
  z-index 4
.city_logo_item:nth-child(11)
  z-index 3
.city_logo_item:nth-child(12)
  z-index 2
</style>
