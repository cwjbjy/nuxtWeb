<template>
  <header class="header">
    <div>
      <div class="title">新闻头条</div>
      <div class="subtitle">https://nuxt.cwjbjy.online</div>
    </div>
  </header>
</template>

<style scoped lang="scss">
.header {
  display: flex;
  justify-content: space-between;
  background: #fff;
  max-width: 1200px;
  margin: 20px auto;
  .title {
    font-size: 32px;
    font-weight: bolder;
    font-style: italic;
    text-align: center;
  }
  .subtitle {
    color: #fe8900;
    font-weight: bold;
  }
  .search {
    display: flex;
    align-items: center;
    width: 380px;
  }
}
</style>
