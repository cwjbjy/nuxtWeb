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
<style>
.el-input__inner {
  border-radius: 0;
  border: 1px solid #fe8900;
}
.el-input-group__append,
.el-input-group__prepend {
  background: #fe8900;
  color: #fff;
  border: 0;
}
</style>
