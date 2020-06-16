<template lang="pug">


  .Slides

    client-only
      agile(
        :dots="false"
        fade

        autoplay
        pause-on-hover
      )
        .slide(
          v-for="It in slides"
          :key="It.id"
        ) 

          img.img_w(
            :src="require(`~/static/img/сities/${It.id}.jpg`)"
          )

          .id
            b {{String(It.id).length === 1 ? `0${It.id}` : It.id}}
            small.text_s2 /12
          img.atom(
            src="~static/icon/atom_w.png"
          )
          
          img.logo(
            :src="require(`~/static/icon/logo_of_сities/${It.id}.png`)"
          )


          .slide_body
            .city {{It.city}}
            .H.my-2 {{It.region}}
            .description {{It.description}}


        template(slot="prevButton") &nbsp;
        template(slot="nextButton") &nbsp;


</template>

<script>
const DATA = [
  {
    id: 1,
    city: 'Глазов',
    region: 'Удмуртская Республика',
    description:
      'Крупнейший изготовитель продукции из циркония, урана, титана и других металлов'
  },
  {
    id: 2,
    city: 'Новоуральск',
    region: 'Свердловская область',
    description:
      'Здесь самое крупное в мире производство по обогащению урана для ядерного топлива, используемого в АЭС'
  },
  {
    id: 3,
    city: 'Саров',
    region: 'Нижегородская область',
    description:
      'Российский федеральный ядерный центр, здесь создается ядерный щит страны'
  },
  {
    id: 4,
    city: 'Железногорск',
    region: 'Красноярский край',
    description:
      'Построенный в скале уникальный комбинат работает над замыканием ядерного топливного цикла'
  },

  {
    id: 5,
    city: 'Заречный',
    region: 'Свердловская область',
    description:
      'Здесь – единственные в России и крупнейшие в мире энергоблоки с реакторами на быстрых нейтронах'
  },
  {
    id: 6,
    city: 'Заречный',
    region: 'Пензенская область',
    description:
      'Производит уникальную высокотехнологичную продукцию для укрепления обороноспособности страны'
  },
  {
    id: 7,
    city: 'Лесной',
    region: 'Свердловская область',
    description:
      'Производит стабильные изотопы, счетчики Гейгера, изделия спецназначения для российской армии'
  },
  {
    id: 8,
    city: 'Озёрск',
    region: 'Челябинская область',
    description:
      'Обеспечивает безопасность страны, перерабатывает отработавшее ядерное топливо, производит изотопы'
  },
  {
    id: 9,
    city: 'Северск',
    region: 'Томская область',
    description:
      'Производит обогащенный уран для ядерного топлива, используемого в АЭС'
  },
  {
    id: 10,
    city: 'Снежинск',
    region: 'Челябинская область',
    description:
      'Российский федеральный ядерный центр, здесь создаются ядерные заряды для мирных и оборонных целей'
  },
  {
    id: 11,
    city: 'Трёхгорный',
    region: 'Челябинская область',
    description:
      'Производит сложнейшую микроэлектронику, электроавтоматику, системы радиационного контроля'
  },
  {
    id: 12,
    city: 'Зеленогорск',
    region: 'Красноярский край',
    description:
      'Один из крупнейших в мире производителей изотопов для ядерной медицины'
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

.Slides
  position absolute
  z-index 10
  top 0
  right 0

  width:360px
  height 450px

.agile
  // &__list
  //   shadow()
  &__actions
    top: 240px;
    // flex-direction: column;
    right: 10px;
    position: absolute;
  &__nav-button
    padding 0
    margin-left 10px
    circle(50px)
    box-shadow: 0px 1px 2px rgba(0, 0, 0, 0.18), 0px 1px 2px rgba(0, 0, 0, 0.04), 0px 2px 6px rgba(0, 0, 0, 0.04);

    &:hover
      box-shadow: 0px 1px 2px rgba(0, 0, 0, 0.18), 0px 1px 2px rgba(0, 0, 0, 0.04), 0px 1px 10px rgba(0, 0, 0, 0.3);


    &--prev
      background url("~static/icon/L.png") no-repeat center
    &--next
      background url("~static/icon/R.png") no-repeat center




.slide
  // box-shadow: 0px 1px 2px rgba(0, 0, 0, 0.18), 0px 1px 7px rgba(0, 0, 0, 0.13), 0px 2px 20px rgba(0, 0, 0, 0.13);
  // shadow()
  background: #FFF;
  height 400px
  margin-top 50px
  position relative


  &_body
    padding 1em
    padding-right 130px
    // shadow()


  .id, .atom, .logo
    position absolute


  .logo
    // circle(100px)
    // background #000
    top -50px
    right 1em

  .id
    top 1em
    left 1em
    color #fff
    font-size 2em
  .atom
    left 1.6em
    top 6em
  .city
    color $blue_l
    font-size 2em
    font-weight  bold
  // .region
  // .description
</style>
