<template>
  <article>
    <Card :url="'/junshi.png'" :source="List">最新军事</Card>
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
      type: "junshi",
      key: store.state.key,
    };
    let { data } = await app.$axios("/toutiao/index", { params: params });
    return {
      List: data.result.data,
    };
  },
  head() {
    return {
      title: "最新军事",
      meta: [
        {
          name: "description",
          hid: "description",
          content: "最新军事，获取最新军事",
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
