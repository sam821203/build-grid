<template>
  <section class="build__wrap layout--main card--6n1bn01">
    <div class="item__wrap">
      <build-item v-for="item in buildItems" :key="item.id" :img-url="item.imgUrL"></build-item>
    </div>
  </section>
</template>

<script>
import BuildItem from '../UI/BuildItem.vue'

export default {
  components: {
    BuildItem
  },
  setup () {
    const buildItems = [
      {
        id: 'a1',
        name: 'Maximilian',
        description:
            "I'm Maximilian and I've worked as a freelance web developer for years. Let me help you become a developer as well!",
        price: 30,
        imgUrL: 'https://media.etmall.com.tw/NXimg/006253/6253344/6253344-1_L.jpg'
      },
      {
        id: 'a2',
        name: 'Julie',
        description:
            'I am Julie and as a senior developer in a big tech company, I can help you get your first job or progress in your current role.',
        price: 3000,
        imgUrl: 'https://media.etmall.com.tw/NXimg/004678/4678312/4678312-1_L.jpg'
      }
    ]

    return {
      buildItems
    }
  }
}
</script>

<style scoped>
.build__wrap {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around;
}
.build__wrap .item__wrap {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  width: 100%;
  padding-left: 10px;
  padding-right: 10px;
}
</style>
