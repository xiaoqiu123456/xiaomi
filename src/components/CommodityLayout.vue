<template>
<div class="commodity-layout">
  <div class="commodity-left">
    <slot name="left"></slot>
  </div>
  <div class="commodity-right">
    <slot name="right"></slot>
  </div>
</div>
</template>

<script>
export default {
  name: "CommodityLayout"
}
</script>

<style lang="less">
.commodity-layout{
  display: flex;
}
.commodity-left{
  width: 234px;
  /*background-color: #9a6e3a;*/
}

.commodity-right{
  margin-left: 14px;
  flex: 1;
  display: flex;
  flex-wrap: wrap;
  .small-img{
    margin-left: 14px;
    margin-top: 14px;
    &:nth-child(4n+1) {
      margin-left: 0;
    }
    &:nth-child(-n+4){
      margin-top: 0;
    }
  }
  /*background-color: #42b983;*/
}
</style>