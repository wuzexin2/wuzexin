<template>
  <div class="header">
    <div class="head-left el-icon-arrow-left"></div>
    <div class="head-input">
      <el-input v-model="input"  prefix-icon="el-icon-search" placeholder="输入城市/游玩景点/主题"></el-input>
    </div>
    <div class="head-right">
      <el-select v-model="value" placeholder="请选择">
        <el-option v-for="item in cities" :key="item.value" :label="item.label" :value="item.value">
          <span style="float: left">{{ item.label }}</span>
          <span style="float: right; color: #8492a6; font-size: 13px">{{ item.value }}</span>
        </el-option>
      </el-select>
    </div>
  </div>
</template>
<script>
export default {
  name: "HomeHeader",
  data() {
    return {
      input: "",
      cities: [
        {
          value: "Beijing",
          label: "北京"
        },
        {
          value: "Shanghai",
          label: "上海"
        },
        {
          value: "Nanjing",
          label: "南京"
        },
        {
          value: "Chengdu",
          label: "成都"
        },
        {
          value: "Shenzhen",
          label: "深圳"
        },
        {
          value: "Guangzhou",
          label: "广州"
        }
      ],
      value: ""
    };
  }
};
</script>
<style scoped>
.header {
display: flex;
  height: 50px;
  background-color: lightseagreen;
  justify-content: space-around;
  width:640px;
  max-width: 640px;
  box-sizing: border-box;
  margin: 0 auto;
}
.head-left {
    
    text-align: center;
    line-height: 50px;
    color: #fff;
}
.head-input {
    width: 70%;
    text-align: center;
    line-height: 50px;
    color: #fff;
}
.head-right {
    width: 20%;
    text-align: right;
    right:0px;
    line-height: 50px;
    color: #fff;

}
</style>