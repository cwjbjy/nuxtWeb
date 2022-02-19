<template>
  <nav class="menu">
    <ul style="list-style-type: none">
      <nuxt-link
        v-for="(item, index) in menus"
        :key="index"
        :to="item.path"
        exact
        tag="li"
        active-class="router_focus"
      >
        <span>{{ item.name }}</span>
      </nuxt-link>
    </ul>
  </nav>
</template>

<script>
export default {
  data() {
    return {
      menus: [
        {
          name: "首页",
          path: "/",
        },
        {
          name: "社会",
          path: "/society",
        },
        {
          name: "国内",
          path: "/inland",
        },
        {
          name: "国际",
          path: "/international",
        },
        {
          name: "娱乐",
          path: "/recreation",
        },
        {
          name: "体育",
          path: "/sports",
        },
        {
          name: "军事",
          path: "/military",
        },
      ],
    };
  },
};
</script>

<style scoped lang="scss">
.menu {
  max-width: 1200px;
  margin: 0 auto;
}
ul {
  display: flex;
  margin: 0;
  padding: 0;
  height: 60px;
  font-size: 18px;
  color: #fff;
  li {
    height: 60px;
    line-height: 60px;
    margin: 0;
    padding: 0 20px;
    cursor: pointer;
  }
}
.router_focus {
  color: #ffd04b;
  border-bottom: 3px solid;
  box-sizing: border-box;
}
</style>
