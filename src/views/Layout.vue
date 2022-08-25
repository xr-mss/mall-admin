<template>
  <div>
    <el-container style="height: 100%">
      <el-aside style="height: 100%">
        <SideBar></SideBar>
      </el-aside>
      <el-container>
        <el-header>Header</el-header>
        <el-main>Main</el-main>
      </el-container>
    </el-container>
  </div>
</template>

<style></style>

<script>
import SideBar from "./Layout/SideBar.vue";
export default {
  data() {
    const item = {
      date: "2016-05-02",
      name: "王小虎",
      address: "上海市普陀区金沙江路 1518 弄",
    };
    return {
      tableData: Array(20).fill(item),
    };
  },
  components: {
    SideBar,
    SideBar,
  },
};
</script>
