<template>
    <div class="recommend">
        <div class="header">
            热销推荐
        </div>
        <ul>
            <li class="item border-botton" v-for="item in recommendList" :key="item.id">
                
                    <img class="item-img-content" :src="item.imgUrl">
                
                <div class="item-info">
                    <p class="item-title">{{item.title}}</p>
                    <p class="item-desc">{{item.desc}}</p>
                    <button class="item-button">查看详情</button>
                </div>
            </li>
        </ul>
    </div>
</template>
<script>
export default {
    name:'HomeRecommend',
    data(){
        return{
            recommendList:[
                {
                    'id':'1',
                    'imgUrl':'../../../static/images/rm1.jpg',
                    'title':'桂林两江四湖景区',
                    'desc':'国内著名旅游景点'
                },
                {
                    'id':'2',
                    'imgUrl':'../../../static/images/rm2.jpg',
                    'title':'南京阅江楼',
                    'desc':'中国十大文化名楼之一，也是江南四大名楼之一，也是南京阅江楼景区的主要景点，有“江南第一楼”之称。'
                },
                {
                    'id':'3',
                    'imgUrl':'../../../static/images/rm3.jpg',
                    'title':'九寨沟',
                    'desc':'“九寨归来不看水”，是对九寨沟景色真实的诠释'
                },
                {
                    'id':'4',
                    'imgUrl':'../../../static/images/rm4.jpg',
                    'title':'庐山瀑布',
                    'desc':'飞流直下三千尺，疑是银河落九天'
                },
                {
                    'id':'5',
                    'imgUrl':'../../../static/images/rm5.jpg',
                    'title':'深圳夜景',
                    'desc':'夜灯下的深圳繁华安谧'
                },
            ]
        }
    }
}
</script>
<style scoped>
.recommend{
 width:640px;
  max-width: 640px;
  box-sizing: border-box;
   margin: 0 auto;
}
 .header {
    margin-top: 10px;
    padding-left:40px;
    line-height: 45px;
    height: 45px;
    background-color: #eeeeee;
}
.item{
    display: flex;
    list-style: none;
    flex:1;
    margin-bottom: 10px;
    box-shadow: -2px -2px 5px #065EAF;
}
.item-info{
   width: 60%;
   height: 263px;
   margin-left: 10px;
  position: relative;
}
.item-img-content{
    width:40%;
}
 .item-info .item-title{
     font-size: 2em;
 }
 .item-info .item-desc{
     font-size: 1em;
     color:#ccc;
     margin-top: 10px;
 }
 .item-info .item-button{

padding: 0.15em;
background-color: #ff9300;
font-size: 1.2em;
color: #fff;
border-radius: 10px;
position: absolute;
bottom:30px;


 }
</style>