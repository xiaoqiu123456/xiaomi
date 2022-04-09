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

<style scoped>
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
  /*background-color: #42b983;*/
}
</style>