<template lang="pug">
.TopLine
  .wrap
    .upper.flex.x_sb.y_center
      .flex.y_center(
        v-scroll-to="'#Form'"
      )
        img(
          src="~static/icon/LOGO.png"
        )
        .ml-3 умные города
          br
          | Росатома
      .flex.y_center.bold
        .scrollTo(
          v-scroll-to="'#Cities'"
        ) Города
        .scrollTo.mx-5(
          v-scroll-to="'#Capabilities'"
        ) Возможности
        .scrollTo(
          v-scroll-to="'#Form'"
        ) Подать заявку

    .center
      img(
        src="~static/icon/atom.svg"
      )
</template>

<script>
export default {}
</script>

<style lang="stylus">
.scrollTo
  cursor pointer
.TopLine
  position absolute
  top 1em
  left 1em
  right 1em
  z-index 10
  // width 100%
</style>
