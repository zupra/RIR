<template lang="pug">

.Footer.wrap.flex_wr.x_sb
  div
    h2 Контакты
    .H АО «Русатом Инфраструктурные решения»
    p.mb-3 г. Москва, Погорельский переулок, д 7, ст 2

    img(src='~static/icon/footer_1.png')
    img.ml-4(src='~static/icon/footer_2.png')

  div
    .bold.text_x4 +7 (495) 357 00 14

  div
    h2 Поделиться в соцсетях
    .flex.socialsIcon
      .icon
      .icon
      .icon
      .icon


</template>

<script>
export default {}
</script>

<style lang="stylus">
.Footer
  padding 5em 1em
  color: $header;

.socialsIcon
  .icon
    shadow()
    margin-right 2em
    // background-color #FFF
    background-position center
    background-repeat no-repeat
    &:nth-of-type(1)
      background-image url("~static/icon/socials/vk base.png")
    &:nth-of-type(2)
      background-image url("~static/icon/socials/fb base.png")
    &:nth-of-type(3)
      background-image url("~static/icon/socials/yt base.png")
    &:nth-of-type(4)
      background-image url("~static/icon/socials/inst base.png")
</style>
