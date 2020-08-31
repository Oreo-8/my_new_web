<template>
  <div id="mainindex">
    <a-layout>
      <a-layout-header class="i-header">
        <a-row style="height: 100%;">
          <a-col class="col-1" :span="12">col-12</a-col>
          <a-col class="col-2" :span="12">
            <navigation-bar class="n-bar" />
          </a-col>
        </a-row>
      </a-layout-header>
      <a-layout-content>
        <router-view />
      </a-layout-content>
      <a-layout-footer>Footer</a-layout-footer>
    </a-layout>
  </div>
</template>
<script>
import navigationBar from "@/components/navigationBar";
export default {
  components: {
    navigationBar,
  },
  data() {
    return {};
  },
};
</script>
<style scoped>
.i-header {
  padding: 0;
}
.col-1 {
  height: 100%;
}
.col-2 {
  height: 100%;
  position: relative;
}
.n-bar {
  position: absolute;
  bottom: 0;
  width: 100%;
}
</style>