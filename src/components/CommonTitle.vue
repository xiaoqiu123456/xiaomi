<template>
<div class="common-title">
  <h2 class="title">{{ title }}</h2>
  <div class="more">
    <p>更多</p>
    <span class="iconfont icon-quanquanxiangyoujiantou"></span>
  </div>
</div>
</template>

<script>
export default {
  name: "CommonTitle",
  props: {
    title: String,
  }
}
</script>

<style scoped lang="less">
  .common-title{
    display: flex;
    justify-content: space-between;
    align-items:center;
    height: 58px;
    -webkit-font-smoothing: antialiased;
    .title{
      margin: 0;
      font-size: 22px;
      font-weight: 200;
      line-height: 58px;
      color: #333;
    }
    .more{
      display: flex;
      align-items: center;
      font-size: 16px;
      line-height: 58px;
      color: #424242;
      -webkit-transition: all .4s;
      transition: all .4s;
      cursor: pointer;
      &:hover{
        color: #ff6700;
      }
      .iconfont{
        font-size: 18px;
        margin-left: 6px;
        padding: 4px;
      }
    }

  }
</style>