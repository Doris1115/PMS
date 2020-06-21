<template>
  <el-menu
    class="el-menu-vertical-demo"
    text-color="#fff"
    active-text-color="#fff"
    background-color="#253443"
    unique-opened
  >
    <el-submenu :index="index" v-for="(item, index) in items" v-bind:key="index">
      <template slot="title">
        <i class="el-icon-message"></i>{{item.F_FullName}}
      </template>
      <el-menu-item-group>
        <el-menu-item v-for="(child,childIndex) in item.ChildNodes"  v-bind:key="childIndex">{{child.F_FullName}}</el-menu-item>
      </el-menu-item-group>
    </el-submenu>
    
  </el-menu>
</template>

<style>
.el-submenu {
  background: #253443;
}
</style>
<script>
import axios from "axios";
export default {
  name: "SlideBar",
  data: function() {
    return {
      items: []
    };
  },
    mounted() {
      this.getData();
    },
  methods: {
    getData() {
      axios.get("/json/GetClientsDataJson.json", {}).then(response => {
          this.items = response.data.authorizeMenu;
        console.log(this.items);
      });
    }
  }
};
</script>