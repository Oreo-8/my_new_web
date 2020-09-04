<template>
  <div id="my-bar">
    <a-menu v-model="current" mode="horizontal" theme="dark">
      <a-menu-item key="mail">
        <a-icon type="home" />主页
      </a-menu-item>
      <a-menu-item key="mail1">
        <a-icon type="home" />分类
      </a-menu-item>
      <a-menu-item key="mail2">
        <a-icon type="home" />收藏
      </a-menu-item>
      <a-menu-item key="mail3">
        <a-icon type="home" />设置
      </a-menu-item>
      <a-menu-item key="mail4">
        <a-icon type="home" />管理
      </a-menu-item>
    </a-menu>
  </div>
</template>
<script>
export default {
  data() {
    return {
      current: ["mail"],
    };
  },
};
</script>
<style scoped>
</style>