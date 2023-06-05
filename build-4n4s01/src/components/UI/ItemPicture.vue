<template>
  <div class="item__pic">
    <img
      class="item__img lazyload"
      data-src="imgUrL"
      src="imgUrL"
      alt=""
    />
    <div>{{ imgUrl }}</div>
  </div>
</template>

<script>
// import { computed } from 'vue'

export default {
  props: [
    'imgUrl'
  ]
  // setup (props) {
  //   const imgURL = computed(() => {
  //     return props.imgUrl
  //   })

  //   return {
  //     imgURL
  //   }
  // }
}
</script>
