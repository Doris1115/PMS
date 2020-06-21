<template>
  <div class="clearfix">
    <div class="headerBar pull-left">
      <div class="pull-left">
        <el-image
          style="width: 40px; height: 40px"
          src="http://139.9.121.59:8001/Content/images/logo.jpg"
          fit="fit"
        ></el-image>
      </div>
      <h1 class="pull-left">拢鑫窗帘IOT系统</h1>
    </div>
    <div class="pull-right">
      <el-dropdown trigger="hover">
        <i class="el-icon-message user-box"></i>
        <el-dropdown-menu slot="dropdown">
          <el-dropdown-item>个人中心</el-dropdown-item>
          <el-dropdown-item>安全退出</el-dropdown-item>
        </el-dropdown-menu>
      </el-dropdown>
      <el-avatar src="https://cube.elemecdn.com/0/88/03b0d39583f48206768a7534e55bcpng.png"></el-avatar>
    </div>
  </div>
</template>
<script>
export default {
  name: "Header"
};
</script>
<style>
.headerBar {
  margin-top: 10px;
  overflow: hidden;
}
h1 {
  color: #fff;
  font-size: 22px;
  line-height: 40px;
  margin: 0 10px;
}
.el-avatar {
  margin-top: 10px;
}
.user-box {
  font-size: 20px;
  margin-right: 15px;
  color: #fff;
}
</style>