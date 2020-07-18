<template>
  <div class="recommend">
    <div v-for="item in recommend" class="recommend-item">
      <a :href="item.link">
        <img :src="item.image">
        <div>{{item.title}}</div>
      </a>
    </div>
  </div>
</template>
<script>
  export default {
    name: "RecommendView",
    props: {
      recommend: {
        type: Array,
        default() {
          return [];
        }
      }

    }
  }
</script>

<style scoped>
  .recommend {
    display: flex;
    width: 100%;
    text-align: center;
    border-bottom: 7px solid #eee;
  }

  .recommend-item {
    flex: 1;
    font-size: 15px;
    padding: 10px 0px 25px;

  }
  .recommend-item img{
    height: 75px;
    width: 75px;
    margin-bottom: 10px;

  }


</style>
