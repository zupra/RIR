<template lang="pug">
section
  h2.H Разработчики
  .flex.y_center
    .text_x1 АО «Русатом Инфраструктурные решения» — компания-интегратор решений Росатома для создания комфортной жизни в городе.
    .btn Перейти на сайт компании
  .scrollList.p-2
    .Card.p-4(
      v-for="_,idx in Array(12)"
    )
      .text_x1.mb-3 Проект Платформа «Умный город»
      p Veniam, id minima sequi nulla, adipisci ullam repudiandae esse iste deleniti eius eveniet? Maiores fugit delectus provident quos sequi veritatis dolor eligendi!

      .bold.mt-3(
        style="color: #2D71F7;"
      ) Смотреть проект
</template>

<script>
export default {
  name: 'Developers'
}
</script>

<style lang="stylus" scoped></style>
