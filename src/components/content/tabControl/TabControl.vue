<template>
<div class="tabcontrol">
  <div v-for="(item,index) in titles" class="tabcontrol-item" :class="{active:index===currentIndex}" @click="itemClick(index)">
    <span>{{item}}</span>
  </div>
</div>



</template>

<script>
  export default {
    name: "TabControl",
    props: {
      titles: {
        type: Array,
        default() {
          return []
        }
      }
    },
    data(){
      return{
        currentIndex:0
      }
    },
    methods:{
      itemClick(index){
        this.currentIndex=index;
        this.$emit('tabClick',index)
      }



    }
  }
</script>

<style scoped>
.tabcontrol{
  display: flex;
  text-align: center;
  font-size: 15px;
  height:40px;
  line-height: 40px;
  background-color: #fff;

}
  .tabcontrol-item{
    flex: 1;

  }

  .active span{

    color: rgba(255, 148, 145, 1);
    border-bottom: 2px solid rgba(255, 148, 145, 1);
    padding: 5px;
  }

</style>
