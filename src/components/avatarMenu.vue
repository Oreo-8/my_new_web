<template>
  <a-dropdown>
    <a-menu slot="overlay" @click="handleMenuClick">
      <!-- v-fro 遍历 -->
      <a-menu-item key="1">
        <a-icon type="user" />1st menu item
      </a-menu-item>
      <a-menu-item key="2">
        <a-icon type="user" />2nd menu item
      </a-menu-item>
      <a-menu-item key="3">
        <a-icon type="user" />3rd item
      </a-menu-item>
    </a-menu>
    <a-avatar
      shape="square"
      size="large"
      :style="{ backgroundColor: color, verticalAlign: 'middle' }"
    >{{ avatarValue }}</a-avatar>
  </a-dropdown>
</template>
<script>
const colorList = ["#f56a00", "#7265e6", "#ffbf00", "#00a2ae"];
export default {
  data() {
    return {
      avatarValue: "未登录",
      color: "#1890ff",
    };
  },
};
</script>