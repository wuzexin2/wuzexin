<template>
  <div class="swiper-container lcons">
     
    <div class="swiper-wrapper"  >
        <div class="swiper-slide"  >
            <img src="../../../static/images/ico1.jpg"/>
            <p class="icon-desc">景点门票</p>
        </div>
        <div class="swiper-slide"  >
            <img src="../../../static/images/ico2.jpg"/>
            <p class="icon-desc">滑雪季</p>
        </div>
        <div class="swiper-slide"  >
            <img src="../../../static/images/ico3.jpg"/>
            <p class="icon-desc">泡温泉</p>
        </div>
        <div class="swiper-slide"  >
            <img src="../../../static/images/ico4.jpg"/>
            <p class="icon-desc">动植园</p>
        </div>
        <div class="swiper-slide"  >
            <img src="../../../static/images/ico5.jpg"/>
            <p class="icon-desc">游乐园</p>
        </div>
        <div class="swiper-slide"  >
            <img src="../../../static/images/ico6.jpg"/>
            <p class="icon-desc">必游榜单</p>
        </div>
        <div class="swiper-slide"  >
            <img src="../../../static/images/ico7.jpg"/>
            <p class="icon-desc">演出</p>
        </div>   
        <div class="swiper-slide"  >
            <img src="../../../static/images/ico8.png"/>
            <p class="icon-desc">城市观光</p>
        </div>    
    </div>  
    <!-- 如果需要分页器 -->
    <div class="swiper-pagination"></div>
  </div>


</template>
<script>
import Swiper from 'swiper';
import '../../../node_modules/swiper/css/swiper.min.css'

export default {
  name: "Homelcons",
  data() {
    
  },
  mounted(){
      new Swiper('.swiper-container',{
          slidesPerView:4,
          slidesPerColumn:2,
          spaceBetween:30,
          loop:true,
         
        // 如果需要分页器
        pagination: {el:'.swiper-pagination',clickable:true}
      })
  }
 
};
</script>
<style scoped>
@import "../../../node_modules/swiper/css/swiper.min.css";
.lcons{
    width:640px;
  max-width: 640px;
  box-sizing: border-box;
   margin: 0 auto;
}
.swiper-container {
    
   
    padding: 0;
  }

  .swiper-wrapper {
    height: 200px;
  }

  .swiper-slide img {
    max-width: 100%;
  }

.swiper-container .swiper-wrapper .swiper-slide {
    text-align: center;
    background: #fff; 
    align-items: center;
    margin-top: 0px !important;
  }
</style>
</style>