<template>
  <div class="introduction">
    <div class="container">
      <div class="inner">
        <el-button type="info" :autofocus=true @click="toDetail(0)">外联部 / 市场拓展部</el-button>
        <el-button type="info" @click="toDetail(1)">节目部</el-button>
        <el-button type="info" @click="toDetail(2)">人力资源部</el-button>
        <el-button type="info" @click="toDetail(3)">编辑部 / 频道资讯部</el-button>
        <el-button type="info" @click="toDetail(4)">综合新闻部</el-button>
        <el-button type="info" @click="toDetail(5)">行政部 / 综合管理部</el-button>
        <el-button type="info" @click="toDetail(6)">策划推广部 / 形象推广部</el-button>
        <el-button type="info" @click="toDetail(7)">视觉设计部</el-button>
        <el-button type="info" @click="toDetail(8)">技术部</el-button>
        <el-button type="info" @click="toDetail(9)">视频部</el-button>
      </div>
    </div>
    <div class="bottom-pic" style="position:absolute;bottom:0">
      <img src="../assets/3.png" style="width:100%;vertical-align: bottom;" />
    </div>
  </div>
</template>

<script>
import { wxshare } from "../api/api";
export default {
  name: "introduction",
  methods: {
    toDetail(i) {
      this.$router.push({
        name: "detail",
        params: {
          i: i
        }
      });
    }
  },
  mounted: function() {
    wxshare(this)
  }
};
</script>

<style>
/* element组件与sibling兄弟选择器的问题 */
.introduction {
  background-color: #f2f7dc;
  height: 100%;
    width: 100%;
    position: absolute;
    top: 0;
}
.introduction .container {
  height: 72.3%;
  width: 100%;
  padding-top: 12.7%;
    overflow: scroll;
}
.introduction .container .inner{
  display: flex;
  flex-direction: column;
  justify-content: center;
}
.el-button--info {
  margin: 20px auto;
  width: 50%;
}
.el-button {
  border: #89c997 solid 1px;
  color: #89c997;
  background-color: transparent;
  width: 50%;
  border-radius: 9pt;
  margin-left: auto !important;
}
.el-button:hover,.el-button:active,.el-button:focus {
  background-color: #89c997;
  color: #ffffff;
  outline: none;
}
</style>