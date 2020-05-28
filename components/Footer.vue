<template lang="pug">

.Footer.wrap

  .flex_wr.x_sb
    div
      h2 Контакты
      .H АО «Русатом Инфраструктурные решения»
      p.mb-3 г. Москва, Погорельский переулок, д 7, ст 2

    div
      .bold.text_x4.my-1 +7 (495) 357 00 14

      a.link(
        href="mailto:info@rusatom-utilities.ru"
      ) info@rusatom-utilities.ru

    div
      h2 Поделиться в соцсетях
      .flex.socialsIcon
        ShareNetwork(
          network="vk"
          url="https://news.vuejs.org/issues/180"
          title="Say hi to Vite! A brand new, extremely fast development setup for Vue."
          description="This week, I’d like to introduce you to 'Vite', which means 'Fast'. It’s a brand new development setup created by Evan You."
          quote="The hot reload is so fast it\'s near instant. - Evan You"
          hashtags="vuejs,vite"
        ) 
          .icon.vk
        ShareNetwork(
          network="facebook"
          url="https://news.vuejs.org/issues/180"
          title="Say hi to Vite! A brand new, extremely fast development setup for Vue."
          description="This week, I’d like to introduce you to 'Vite', which means 'Fast'. It’s a brand new development setup created by Evan You."
          quote="The hot reload is so fast it\'s near instant. - Evan You"
          hashtags="vuejs,vite"
        ) 
          .icon.fb
        .icon.yt
        .icon.inst



  .flex.x_sb.mt-5.y_base
    .flex.y_center
      img(src='~static/icon/footer_1.svg')
      img.ml-4(src='~static/icon/footer_2.svg')
    div
      img(src='~static/icon/app_store.png')
      img.ml-2(src='~static/icon/google_play.png')


</template>

<script>
export default {}
</script>

<style lang="stylus">
.Footer
  // background #FEFFFF
  padding 5em 1em 2em
  color: $header;

.socialsIcon
  .icon
    shadow()
    margin-right 2em
    // background-color #FFF
    background-position center
    background-repeat no-repeat
  .vk
    background-image url("~static/icon/socials/vk base.png")
    &:hover
      background: #01468D url("~static/icon/socials/vk hover.png") center  no-repeat
  .fb
    background-image url("~static/icon/socials/fb base.png")
    &:hover
      background: #3366FF url("~static/icon/socials/fb hover.png") center  no-repeat
  .yt
    background-image url("~static/icon/socials/yt base.png")
    &:hover
      background: #FC0D1B url("~static/icon/socials/yt hover.png") center  no-repeat
  .inst
    background-image url("~static/icon/socials/inst base.png")
    &:hover
      background: url("~static/icon/socials/inst hover.png") center  no-repeat, linear-gradient(211.29deg, #5058CA 19.57%, #D62C78 54.97%, #F5CB6E 89.63%)
</style>
