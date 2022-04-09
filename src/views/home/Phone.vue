<template>
<div class="phone ">
  <CommodityLayout>
    <template v-slot:left>
      <BigImg/>
    </template>
    <template v-slot:right>
      <div>我在右边</div>
    </template>
  </CommodityLayout>
</div>
</template>

<script setup>
import CommodityLayout from "../../components/CommodityLayout.vue";
import BigImg from "../../components/BigImg.vue";

const phoneList = [
  {
    id: 10000,
    imgUrl: '',
    name: '',
    info: '',
    price: 869,
    sourcePrice: 998,
    renderType: 2, // 1大图 2小图 3更多
  }
]
</script>

<style scoped>


</style>