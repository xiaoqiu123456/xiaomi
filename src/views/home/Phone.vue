<template>
  <div class="phone">
    <CommonTitle :title="title" />
    <CommodityLayout>
      <template v-slot:left>
        <BigImg src="https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/ac5cafc68c10ce4471869d378f594b52.png?thumb=1&w=293&h=768&f=webp&q=90"/>
      </template>
      <template v-slot:right>
        <SmallImg v-for="info in phoneList" :key="info.id" :commodityInfo="info" />
      </template>
    </CommodityLayout>
  </div>
</template>

<script setup>
import CommodityLayout from "../../components/CommodityLayout.vue";
import BigImg from "../../components/BigImg.vue";
import SmallImg from "../../components/SmallImg.vue";
import CommonTitle from "../../components/CommonTitle.vue";

const title = '手机'

const phoneList = [
  {
    "link": "https://www.mi.com/redmi10a",
    "id": 10000,
    "imgUrl": "https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/d764150a470174741d8b0b04515f7a78.jpg?thumb=1&w=250&h=250&f=webp&q=90",
    "name": "Redmi 10A",
    "info": "大电量、大音量、大屏幕",
    "sellingPrice": 649,
    "sourcePrice": 699
  },
  {
    "link": "https://www.mi.com/redmik50pro",
    "id": 10001,
    "imgUrl": "https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/18d2099cb0b05bbd23cb1915dfc9d0d6.jpg?thumb=1&w=250&h=250&f=webp&q=90",
    "name": "Redmi K50 Pro",
    "info": "2K直屏的狠旗舰",
    "sellingPrice": 2999,
    "sourcePrice": null
  },
  {
    "link": "https://www.mi.com/redmik50",
    "id": 10002,
    "imgUrl": "https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/28c14106b688ac7ae88e761564789b37.jpg?thumb=1&w=250&h=250&f=webp&q=90",
    "name": "Redmi K50",
    "info": "2K直屏的狠旗舰",
    "sellingPrice": "2399",
    "sourcePrice": null
  },
  {
    "link": "https://www.mi.com/redmik40s",
    "id": 10003,
    "imgUrl": "https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/28febc579eaea6b07c96c0ec48b89f7a.jpg?thumb=1&w=250&h=250&f=webp&q=90",
    "name": "Redmi K40S",
    "info": "口碑真旗舰",
    "sellingPrice": "1799",
    "sourcePrice": null
  },
  {
    "link": "https://www.mi.com/redmik50g",
    "id": 10004,
    "imgUrl": "https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/1061cd8d46977b5291d481d0cd44105e.jpg?thumb=1&w=250&h=250&f=webp&q=90",
    "name": "Redmi K50 电竞版",
    "info": "全线拉满的冷血旗舰",
    "sellingPrice": "3299",
    "sourcePrice": null
  },
  {
    "link": "https://www.mi.com/mi12pro",
    "id": 10005,
    "imgUrl": "https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/a7382271e3a677bf188679ca38d68a42.jpg?thumb=1&w=250&h=250&f=webp&q=90",
    "name": "Xiaomi 12 Pro",
    "info": "全新骁龙8｜2K AMOLED屏幕",
    "sellingPrice": "4699",
    "sourcePrice": null
  },
  {
    "link": "https://www.mi.com/mi12",
    "id": 10006,
    "imgUrl": "https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/e870129c5c374088bf7cc46be0b7ace2.jpg?thumb=1&w=250&h=250&f=webp&q=90",
    "name": "Xiaomi 12",
    "info": "全新骁龙8｜5000万主摄",
    "sellingPrice": "3699",
    "sourcePrice": null
  },
  {
    "link": "https://www.mi.com/mi12x",
    "id": 10007,
    "imgUrl": "https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/63e15f377e87212d460592b4a1369ccd.jpg?thumb=1&w=250&h=250&f=webp&q=90",
    "name": "Xiaomi 12X",
    "info": "骁龙870｜5000万主摄",
    "sellingPrice": "2999",
    "sourcePrice": null
  }
]
</script>

<style scoped>


</style>