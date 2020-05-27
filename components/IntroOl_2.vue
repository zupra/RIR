<template lang="pug" functional>
div
  .flex.y_center.mb-4
    img(
      src="~static/icon/logo_2.png"
    )
    .ml-2.text_x5 РОСАТОМ

  ol
    li 100% российская 
      br 
      | разработка
    li Использует имеющуюся
      br 
      | инфраструктуру
      
    li Адаптируется
      br 
      | под потребности города
</template>

<script>
export default {}
</script>

<style lang="stylus" scoped>
ol
  counter-reset: counter_li;

li
  height 5em
  font-weight bold
  font-size 1.2em


  list-style none
  padding-left 108px
  position relative


  &:before
    position absolute
    left 8px
    // content ''
    color $blue_l
    counter-increment: counter_li;
    content: "0" counter(counter_li);
    font-weight 800
    font-size 1.4rem

    circle(3em)
    line-height 3em
    text-align center

    background #FFF
</style>
