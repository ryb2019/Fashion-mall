<template>
  <div class="goodslist">
    <GoodsListitem v-for="item in goods" :goods-item="item"/>


  </div>
</template>

<script>

  import GoodsListitem from "./GoodsListitem";

  export default {
    name: "GoodsList",
    components: {
      GoodsListitem
    },
    props: {
      goods: {
        type: Array,
        default() {
          return []
        }
      }
    }
  }


</script>

<style scoped>

</style>
