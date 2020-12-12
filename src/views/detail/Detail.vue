<template>
  <div id="detail">
<detail-nav-bar></detail-nav-bar>
    <detail-swiper :top-images="topImages"></detail-swiper>
    <detail-base-info :goods="goods"></detail-base-info>
    <detail-shop-info :shop="shop"></detail-shop-info>
  </div>
</template>

<script>
import DetailNavBar from "./childComps/DetailNavBar"
import DetailSwiper from "./childComps/DetailSwiper"
import DetailBaseInfo from "../home/childComps/DetailBaseInfo"
import DetailShopInfo from "../home/childComps/DetailShopInfo"


import {getDetail,Goods,Shop} from "network/detail"

export default {
    name: "Detail",
    components:{
      DetailNavBar,
      DetailSwiper,
      DetailBaseInfo,
      DetailShopInfo
    },
    data(){
      return{
        iid:null,
        topImage:[],
        goods:{},
        shop:{}
      }
    },
    created() {
      this.iid = this.$route.params.iid
      getDetail(this.iid).then(res =>{
        const  data = res.result;
        this.topImage = data.result.itemInfo.topImages
        this.goods = new Goods(data.itemInfo,data.columns,data.shopInfo.services)
        this.shop = new Shop(data.shopInfo)
      })
    }
  }
</script>

<style scoped>

</style>
