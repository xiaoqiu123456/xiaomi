<template>
  <div class="notebook">
    <CommonTitle title="笔记本|平板"
                 :tabs="[{name: '热门', value: 0}]"/>
    <CommodityLayout>
      <template v-slot:left>
        <BigImg
            src="https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/9895c56a7b792fb9053e3085fc261072.jpg?thumb=1&w=293&h=768&f=webp&q=90"/>
      </template>
      <template v-slot:right>
        <div v-for="(info, index) in list" :key="info.id">
          <CommonMore v-if="index === 7" :common-information="info"/>
          <SmallImg v-else :commodityInfo="info"/>
        </div>
      </template>
    </CommodityLayout>
  </div>
</template>

<script setup>
import CommodityLayout from "../../components/CommodityLayout.vue";
import BigImg from "../../components/BigImg.vue";
import SmallImg from "../../components/SmallImg.vue";
import CommonTitle from "../../components/CommonTitle.vue";
import CommonMore from "../../components/CommonMore.vue";

// 热门
const list = [
  {
    "link": "https://www.mi.com/xiaomiwatchs1",
    "id": 20000,
    "imgUrl": "https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/b8259e8fb355acf168c66f75d375c6af.jpg?thumb=1&w=250&h=250&f=webp&q=90",
    "name": "Xiaomi Watch S1",
    "info": "腕事具备",
    "sellingPrice": "10490",
    "sourcePrice": "10990"
  },
  {
    "link": "https://www.mi.com/xiaomibuds3",
    "id": 20001,
    "imgUrl": "https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/0b271a074e087848357aa61ae665b214.jpg?thumb=1&w=250&h=250&f=webp&q=90",
    "name": "Xiaomi真无线降噪耳机3",
    "info": "静听好声音",
    "sellingPrice": "4590",
    "sourcePrice": "4990"
  },
  {
    "link": "https://www.mi.com/redmiwatch2",
    "id": 20002,
    "imgUrl": "https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/f84503dbf5adbdf17111c61d4a7cf893.jpg?thumb=1&w=250&h=250&f=webp&q=90",
    "name": "Redmi 手表 2",
    "info": "AMOLED高清大屏",
    "sellingPrice": "3790",
    "sourcePrice": "3990"
  },
  {
    "link": "https://www.mi.com/shouhuan6/nfc",
    "id": 20003,
    "imgUrl": "https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/b28153b80cb2c67564608e56d5c2f3f3.jpg?thumb=1&w=250&h=250&f=webp&q=90",
    "name": "小米手环6 NFC版",
    "info": "全屏实力",
    "sellingPrice": "2390",
    "sourcePrice": "2790"
  },
  {
    "link": "https://www.mi.com/redmi-watch-mulan",
    "id": 20004,
    "imgUrl": "https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/cfec307342eb35ee4a437f664004c50f.jpg?thumb=1&w=250&h=250&f=webp&q=90",
    "name": "Redmi 手表",
    "info": "35g超轻/1.4 大屏 / 多功能NFC / 7天长续航", "sellingPrice": "2990", "sourcePrice": null
  },
  {
    "link": "https://www.mi.com/xiaomibuds3pro",
    "id": 20005,
    "imgUrl": "https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/0cc4e8e58d7288cd8dff13b98bdc3ea8.jpg?thumb=1&w=250&h=250&f=webp&q=90",
    "name": "Xiaomi 真无线降噪耳机 3 Pro",
    "info": "动态降噪 静听曼妙",
    "sellingPrice": "6990",
    "sourcePrice": null
  },
  {
    "link": "https://www.mi.com/buy?product_id=14903",
    "id": 20006,
    "imgUrl": "https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/11570d5371f16d2d9b19f504e09d01f0.jpg?thumb=1&w=250&h=250&f=webp&q=90",
    "name": "Redmi Buds 3半入耳真无线蓝牙耳机",
    "info": "轻巧半入耳，舒适有天分",
    "sellingPrice": "1990",
    "sourcePrice": null
  },
  {
    "link": "https://www.mi.com/buy?product_id=15217",
    "id": 20007,
    "imgUrl": "https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/2fcf24e40ff09a254857ac8b4ace25b8.jpg?thumb=1&w=125&h=125&f=webp&q=90",
    "name": "Redmi Buds 3 青春版",
    "info": "",
    "sellingPrice": "990",
    "sourcePrice": null
  }
]

</script>

<style scoped>


</style>