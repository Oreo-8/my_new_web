<template>
  <!-- 内容 -->
  <a-card class="card-child" title="主页" :bordered="true" :hoverable="true">
    <a-list
      class="all-list"
      :bordered="true"
      item-layout="vertical"
      :pagination="pagination"
      :data-source="listData"
    >
      <a-list-item slot="renderItem" key="item.title" slot-scope="item, index">
        <template v-for="{ type, text } in actions" slot="actions">
          <span :key="type" v-if="type != 'delete'">
            <a-icon :type="type" style="margin-right: 8px" />
            {{ text }}
          </span>
          <a-button :key="type" type="link" :icon="type" size="small" v-else>删除</a-button>
        </template>
        <img
          slot="extra"
          width="272"
          alt="logo"
          src="https://gw.alipayobjects.com/zos/rmsportal/mqaQswcyDLcXyDKnZfES.png"
        />
        <a-list-item-meta>
          <a slot="title" :href="item.href">{{ item.title }}</a>
          <a-avatar slot="avatar" :src="item.avatar" />
        </a-list-item-meta>
        <div>{{ item.content }}</div>
        <div style="margin-top: 10px;">
          <a-tag color="blue">blue</a-tag>
        </div>
      </a-list-item>
    </a-list>
  </a-card>
</template>
<script>
const listData = [];
for (let i = 0; i < 23; i++) {
  listData.push({
    href: "https://www.antdv.com/",
    title: `作者`,
    avatar: "https://zos.alipayobjects.com/rmsportal/ODTLcjxAfvqbxHnVXCYX.png",
    description:
      "Ant Design, a design language for background applications, is refined by Ant UED Team.",
    content:
      "We supply a series of design principles, practical patterns and high quality design resources (Sketch and Axure), to help people create their product prototypes beautifully and efficiently.",
  });
}
export default {
  data() {
    return {
      listData,
      pagination: {
        onChange: (page) => {
          console.log(page);
        },
        pageSize: 3,
      },
      actions: [
        { type: "calendar", text: "2020-09-13: 17:34:30" },
        { type: "eye", text: "156" },
        { type: "message", text: "2" },
        { type: "delete", text: "" },
      ],
    };
  },
};
</script>
<style scoped>
.card-child {
  padding-left: 10px;
  padding-right: 10px;
}
</style>