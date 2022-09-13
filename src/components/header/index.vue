<template>
  <div class="header-container">
    <div class="left-wrap">
      <img
        :src="logo"
        class="logo"
      >
      <el-menu
        :default-active="activeIndex2"
        class="el-menu"
        mode="horizontal"
        @select="handleSelect"
        text-color="#fff"
        active-text-color="#ffd04b"
      >
        <el-menu-item index="1">
          <img
            :src="dashboardImg"
            alt="Dashboard"
            class="menu-img"
          >
          <span slot="title">Dashboard</span>

        </el-menu-item>
        <el-menu-item index="2">
          <img
            :src="collectionImg"
            alt="collection"
            class="menu-img"
          >
          <span slot="title">Collections</span>
        </el-menu-item>
        <el-menu-item index="3">
          <img
            :src="campaignImg"
            alt="Campaigns"
            class="menu-img"
          >
          <span slot="title">Campaigns</span>
        </el-menu-item>
      </el-menu>
    </div>
    <div class="right-wrap">
      <img :src="notifyImg">
      <div class="account-inner">
        <img :src="accountImg">
        <span>admin</span>
      </div>
    </div>
  </div>
</template>
<script>
import logo from "@/assets/logo.png";
import dashboardImg from "@/assets/icon-dashboard.png";
import collectionImg from "@/assets/icon-Collection.png";
import campaignImg from "@/assets/icon-campaign.png";
import notifyImg from "@/assets/notify.png";
import accountImg from "@/assets/account-logo.png";

export default {
  data() {
    return {
      logo,
      activeIndex2: undefined,
      collectionImg,
      dashboardImg,
      campaignImg,
      notifyImg,
      accountImg,
    };
  },
  methods: {
    handleSelect() {},
  },
};
</script>
<style lang="less" scoped>
@import "@/style/index.less";

.el-menu {
  background-color: @primary-color;
}
.left-wrap,
.right-wrap,
.header-container {
  background-color: #212326;
  height: 60px;
  display: flex;
  align-items: center;
}

.left-wrap {
  flex: 1;
}
.logo {
  width: 45px;
  height: 36px;
  margin-left: 40px;
}
.menu-img {
  margin-right: 6px;
}
.account-inner {
  margin-left: 16px;
}
.account-inner {
  height: 60px;
  line-height: 60px;
  color: #fff;
  align-items: center;
}
</style>