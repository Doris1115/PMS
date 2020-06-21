<template>
  <div id="app">
    <el-container>
      <el-header
        style="background:#253443;
      width: 100%;
      position: fixed;
      top: 0;"
      >
        <Header />
      </el-header>
      <el-container>
        <el-aside
          width="220px"
          style="background:#253443;height: 100%;
      position: fixed;
      top: 60px;"
        >
          <SlideBar />
        </el-aside>
        <el-main style="
      position: fixed;
      top: 60px;left:220px;">
          <router-view></router-view>
        </el-main>
      </el-container>
    </el-container>
  </div>
</template>
<script>
import Header from "@/components/common/Header.vue";
import SlideBar from "@/components/common/SlideBar.vue";
export default {
  components: {
    Header,
    SlideBar
  }
};
</script>
<style>
</style>

