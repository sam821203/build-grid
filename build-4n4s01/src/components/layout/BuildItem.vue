<template>
  <div class="build__item">
    <a href="">
      <div class="item__box">
        <item-picture></item-picture>
        <div class="item__info">
          <item-description></item-description>
          <item-name></item-name>
          <item-price></item-price>
        </div>
      </div>
    </a>
  </div>
</template>

<script>
import ItemPicture from '../UI/ItemPicture.vue'
import ItemDescription from '../UI/ItemDescription.vue'
import ItemName from '../UI/ItemName.vue'
import ItemPrice from '../UI/ItemPrice.vue'

export default {
  // props: [
  //   'imgUrl'
  // ],
  components: {
    ItemPicture,
    ItemDescription,
    ItemName,
    ItemPrice
  }
}
</script>

<style scoped>
.build__item {
  width: calc(50% - 5px);
  margin-bottom: 10px;
  border-radius: 6px;
  background-color: #fff;
  box-shadow: 0 1px 3px 0 rgb(0 0 0 / 20%);
  overflow: hidden;
  transition: all 0.16s;
}

/* hover float */
.build__item.hover--float-sm:active,
.build__item.hover--float-sm:hover {
  transform: translateY(-3px);
  box-shadow: 0 2px 4.5px 0 rgb(0 0 0 / 25%);
}

/* hover scale */
.build__item.hover--scale-xs:active,
.build__item.hover--scale-xs:hover {
  transform: scale(1.03);
}

.build__item.hover--scale-sm:active,
.build__item.hover--scale-sm:hover {
  transform: scale(1.05);
}

/* ===== RWD 960 ===== */
@media screen and (min-width: 960px) {
  .build__item {
    width: calc(25% - 7.5px);
  }
}

.build__item a {
  color: #5d5d5d;
}
</style>
