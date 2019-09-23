<template>
  <div class="wrap">
    <el-carousel :interval="5000" arrow="always" :height="bannerHeight+'px'">
      <el-carousel-item v-for="item in imgList" :key="item.id">
            <img ref="bannerHeight" :src="item.image" class="banner_img" />
      </el-carousel-item>
    </el-carousel>
  </div>
</template>
<script>
export default {
  name: "HomeSwiper",
  data(){
      return{
          imgList:[
              {id:'1',image:'./static/images/pic1.jpg'},
              {id:'2',image:'./static/images/pic2.jpg'},
              {id:'3',image:'./static/images/pic3.jpg'},
              {id:'4',image:'./static/images/pic4.jpg'},
          ],
          bannerHeight:350,
          screeHeight:0,
      }
  },
  methods:{
      setSize:function(){
          this.bannerHeight=400/1920*this.screewidth;
      },

  },
  mounted(){
      this.screeWidth=window.innerWidth;
      this.setSize();
      window.onresize=()=>{
          this.screeWidth=window.innerWidth;
          this.setSize();
      }
    }
}
</script>
<style scoped>
.wrap{
    width:640px;
  max-width: 640px;
  box-sizing: border-box;
   margin: 0 auto;
}
.banner_img{
    width: 100%;
    height:inherit;
}
</style>