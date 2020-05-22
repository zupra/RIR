<template lang="pug">

.Cities.py-5
  .wrap
    h2 Города-участники
    p Умный город — это целая линейка системных решений для городов разного размера и специфики их развития. Сегодня цифровая платформа «Умный город» развёрнута на территории 12 городов:

  .scrollList
    .city_item.center(
      v-for="It in slides"
      :key="It.id"
    )
      .logo
      .H.text_x1 {{It.city}}
      .H.my-3 {{It.region}}
      .btn Подробнее
      
        


</template>

<script>
const DATA = [
  {
    id: 1,
    city: 'Глазов',
    region: 'Удмуртская Республика'
  },
  {
    id: 2,
    city: 'Новоуральск',
    region: 'Свердловская область'
  },
  {
    id: 3,
    city: 'Саров',
    region: 'Нижегородская область'
  },
  {
    id: 4,
    city: 'Железногорск',
    region: 'Красноярский край'
  },

  {
    id: 5,
    city: 'Заречный',
    region: 'Свердловская область'
  },
  {
    id: 6,
    city: 'Заречный',
    region: 'Пензенская область'
  },
  {
    id: 7,
    city: 'Лесной',
    region: 'Свердловская область'
  },
  {
    id: 8,
    city: 'Озёрск',
    region: 'Челябинская область'
  },
  {
    id: 9,
    city: 'Северск',
    region: 'Томская область'
  },
  {
    id: 10,
    city: 'Снежинск',
    region: 'Челябинская область'
  },
  {
    id: 11,
    city: 'Трёхгорный',
    region: 'Челябинская область'
  },
  {
    id: 12,
    city: 'Зеленогорск',
    region: 'Красноярский край'
  }
]

export default {
  data() {
    return {
      slides: DATA
    }
  }
}
</script>

<style lang="stylus">



.Cities
  background #1D3C7A
  color #FFF

.city_item
  margin-top 60px
  position relative
  background #FFF
  padding 70px 0 2em


  .logo
    position absolute
    circle(100px);
    background gold
    top -50px
    left 50%
    transform translateX(-50%)
</style>
