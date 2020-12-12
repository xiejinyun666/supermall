<template>
  <tab-bar>
    <tab-bar-item path="/home" activeColor="black">
      <img slot="item-icon" src="../../../assets/img/tabbar/home.png" alt="">
      <img slot="item-icon-active" src="../../../assets/img/tabbar/home_active.jpeg" alt="">
      <div slot="item-text">首页</div>
    </tab-bar-item>
    <tab-bar-item path="/category" activeColor="blue">
      <img slot="item-icon" src="../../../assets/img/tabbar/category.jpeg" alt="">
      <img slot="item-icon-active" src="../../../assets/img/tabbar/category_active.jpg" alt="">
      <div slot="item-text">分类</div>
    </tab-bar-item>
    <tab-bar-item path="/cart" activeColor="yellow">
      <img slot="item-icon" src="../../../assets/img/tabbar/shopcart.jpeg" alt="">
      <img slot="item-icon-active" src="../../../assets/img/tabbar/shopcart_active.jpeg" alt="">
      <div slot="item-text">购物车</div>
    </tab-bar-item>
    <tab-bar-item path="/profile" activeColor="blue">
      <img slot="item-icon" src="../../../assets/img/tabbar/profile.jpeg" alt="">
      <img slot="item-icon-active" src="../../../assets/img/tabbar/profile_active.jpg" alt="">
      <div slot="item-text">我的</div>
    </tab-bar-item>
  </tab-bar>
</template>

<script>
  import TabBar from 'components/common/tabbar/TabBar'
  import TabBarItem from 'components/common/tabbar/TabBarItem'

  export default {
    name: "MainTabBar",
    components:{
      TabBar,
      TabBarItem
    }
  }
</script>

<style scoped>

</style>
