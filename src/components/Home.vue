<template>
<div class="home">
    <div class="header">首页</div>
    <home-header></home-header>
    <home-swiper></home-swiper>
    <homelcons></homelcons>
    <home-recommend></home-recommend>
    <home-weekend></home-weekend>
</div>
</template>
<script>
import HomeHeader from './views/Header'
import HomeSwiper from './views/Swiper'
import Homelcons from './views/lcons'
import HomeRecommend from './views/Recommend'
import HomeWeekend from './views/Weekend'


export default {
    name:'Home',
    components:{
        HomeHeader,
        HomeSwiper,
        Homelcons,
        HomeRecommend,
        HomeWeekend
    }


}
</script>
<style scoped>
.home{
   width:640px;
  margin: 0 auto;
}
</style>