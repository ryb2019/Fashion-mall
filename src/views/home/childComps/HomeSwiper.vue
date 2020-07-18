<template>
  <Swiper>
    <Swiper-item v-for="item in banners">
      <a :href="item.link">
        <img :src="item.image">
      </a>
    </Swiper-item>
  </Swiper>
</template>

<script>
  export default {
    name: "HomeSwiper",
    components: {
      SwiperItem,
      Swiper

    },
    props: {
      banners: {
        type: Array,
        default() {
          return []
        }

      }


    }
  }

  import SwiperItem from "../../../components/common/swiper/SwiperItem";
  import Swiper from "../../../components/common/swiper/Swiper";


</script>

<style scoped>

</style>
