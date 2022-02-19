<template>
  <article>
    <Card :url="'/shehui.png'" :source="List">最新社会</Card>
  </article>
</template>

<script>
export default {
  data() {
    return {
      List: [],
    };
  },
  async asyncData({ store, app }) {
    let params = {
      type: "shehui",
      key: store.state.key,
    };
    let { data } = await app.$axios("/toutiao/index", { params: params });
    return {
      List: data.result.data,
    };
  },
  head() {
    return {
      title: "最新社会",
      meta: [
        {
          name: "description",
          hid: "description",
          content: "最新社会，获取社会新闻",
        },
      ],
    };
  },
};
</script>

<style>
article {
  max-width: 1200px;
  margin: 15px auto;
  background: #fff;
}
</style>
