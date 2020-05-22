<template lang="pug">
section
  .capabilities
    .center
      h1 Возможности
      p.mt-3 Базовая платформа «Умный город» —  единая информационная основа для внедрения цифровых городских сервисов. Технологии «Умного города» повышают эффективность управления городскими процессами, облегчая жизнь и горожанам, и властям, расширяя возможность обратной связи.
    .BR
    .flex_wr.x_sb
      div
        h3.H Для жителей
        ul
          li Сообщайте о городских проблемах
          li Отслеживайте работу городских служб
          li Узнавайте о работе муниципальных,
            br
            | образовательных и культурных учреждений
      div
        h3.H Для муниципалитетов
        ul
          li Настройте диалог между жителями и властью
          li Улучшайте процессы взаимодействия с жителями
          li Повышайте эффективность работы городских служб
</template>

<script>
export default {
  name: 'Capatibilities'
}
</script>

<style lang="stylus" scoped>
.capabilities
  .center
    max-width 750px
    margin 0 auto
    line-height 1.6
    font-size 1.2em
  h1
    color: $blue_l
    font-size: 80px;

  li
    padding-left 2.1em
    margin 1em 0
    list-style none
    position relative

    &:before
      position absolute
      left 0
      content ''
      width 1em
      height 1em
      border-radius 50%
      background $blue_l
</style>
