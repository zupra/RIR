<template lang="pug">
section
  h2.H Новости проекта
  .scrollList
    div(
      v-for="_,idx in Array(12)"
    )
      img(
        :src="`https://picsum.photos/id/${idx+10}/300/200`"
      )
      .flex.y_center
        img(
          src="https://icongr.am/octicons/calendar.svg?size=24"
        )
        | &emsp;
        span 30 июл. 2020
      p.mt-2 Приглашаем Вас поделиться мнением и принять участие в «Опросе о работе общественного транспорта в Нижегородской области» …
</template>

<script>
export default {}
</script>

<style lang="stylus" scoped></style>
