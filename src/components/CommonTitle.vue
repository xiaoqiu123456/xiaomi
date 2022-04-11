<template>
<div class="common-title">
  <h2 class="title">{{ title }}</h2>
  <div class="tabs" v-if="tabs.length > 0">
    <a :class="{tab: true, current: tab.value === current}"
       v-for="(tab) in tabs"
       @mouseenter="() => onMouseenter(tab)">
      {{tab.name}}
    </a>
  </div>
  <div class="more" v-else>
    <p>更多</p>
    <span class="iconfont icon-quanquanxiangyoujiantou"></span>
  </div>
</div>
</template>

<script>
// vue2
export default {
  name: "CommonTitle",
  props: {
    tabs: {
      type: Array,
      default: [],
    },
    title: String,
  },
  // 数据
  data() {
    return {
      // 当前选择的标签页
      current: 0
    }
  },
  // 方法
  methods: {
    // 鼠标经过事件
    onMouseenter: function (tab) {
      this.current = tab.value;
      // 自定义事件
      this.$emit('change', tab)
    }
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
    .tabs{
      .tab{
        display: inline-block;
        color: #424242;
        margin-left: 30px;
        border-bottom: 2px solid rgba(0,0,0,0);
        font-size: 16px;
        transition: all .3s;
        cursor: pointer;
        &.current{
          color: #ff6700;
          border-bottom-color: #ff6700;
        }
      }
    }

  }
</style>