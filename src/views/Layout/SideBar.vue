<template>
  <div style="height: 100%">
    <el-menu
      style="height: 100%"
      background-color="#545c64"
      text-color="#fff"
      active-text-color="#ffd04b"
    >
      <template v-for="(item, index) in menus">
        <el-submenu v-if="item.isSubMenu" :key="index">
          <template slot="title">
            <i :class="`el-icon-${item.icon}`"></i>
            <span slot="title">{{ item.title }}</span>
          </template>
          <el-menu-item
            v-for="(subItem, subIndex) in item.children"
            :key="subIndex"
          >
            <i :class="`el-icon-${subItem.icon}`"></i>
            <span slot="title">{{ subItem.title }}</span>
          </el-menu-item>
        </el-submenu>
        <el-menu-item v-else :key="index">
          <i :class="`el-icon-${item.icon}`"></i>
          <span slot="title">{{ item.title }}</span>
        </el-menu-item>
      </template>
    </el-menu>
  </div>
</template>

<script>
export default {
  data() {
    return {
      menus: [
        {
          title: "首页",
          icon: "s-home",
          path: "/",
          isSubMenu: false,
          children: [],
        },
        {
          title: "用户管理",
          icon: "s-custom",
          path: "/user",
          isSubMenu: false,
          children: [],
        },
        {
          title: "商品管理",
          icon: "s-goods",
          path: "/goods",
          isSubMenu: true,
          children: [
            {
              title: "商品列表",
              icon: "s-custom",
              path: "/goods/list",
              isSubMenu: false,
            },
            {
              title: "商品上架",
              icon: "s-custom",
              path: "/goods/create",
              isSubMenu: false,
            },
            {
              title: "商品评论",
              icon: "s-custom",
              path: "/goods/comment",
              isSubMenu: false,
            },
          ],
        },
        {
          title: "推广管理",
          icon: "s-custom",
          path: "/tuiguang",
          isSubMenu: false,
          children: [],
        },
        {
          title: "系统设置",
          icon: "s-custom",
          path: "/system",
          isSubMenu: false,
          children: [],
        },
      ],
    };
  },
  methods: {
    handleOpen(key, keyPath) {
      console.log(key, keyPath);
    },
    handleClose(key, keyPath) {
      console.log(key, keyPath);
    },
  },
};
</script>
<style></style>
