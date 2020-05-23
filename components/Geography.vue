<template lang="pug">
section
  h2.H География
  .MAP
    .num.num_bg 12

    .H.upper.text_x3 АТОМНЫХ ГОРОДОВ
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
import Slides from '~/components/Slides.vue'
export default {
  components: {
    Slides
  }
}
</script>
<style lang="stylus" scoped></style>
