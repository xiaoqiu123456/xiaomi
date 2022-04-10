<template>
<div class="small-img">
  <a :href="commodityInfo.link">
    <card class="card">
      <img :src="commodityInfo.imgUrl" alt="">
      <h6 class="name">{{ commodityInfo.name }}</h6>
      <p class="vice-name">{{commodityInfo.info}}</p>
      <div class="price">
        <p class="selling-price">{{commodityInfo.sellingPrice}}元起</p>
        <p class="original-price">{{commodityInfo.sourcePrice}}元</p>
      </div>
    </card>
  </a>
</div>
</template>

<script>
import Card from "./Card.vue";
// vue2的组件语法
export default {
  // 组件名称
  name: "SmallImg",

  // 注册组件
  components: {
    'card': Card
  },

  // props 组件的输入值（可输入js数据类型）
  props: {
    commodityInfo: Object
  }

}
</script>

<style lang="less" >
.small-img{
  .card{
    padding: 20px 0;
  }
  img{
    display: block;
    width: 160px;
    height: 160px;
    margin: 0 auto 18px;

  }
  .name{
    text-align: center;
    text-overflow: ellipsis;
    white-space: nowrap;
    overflow: hidden;
    margin: 0 10px 2px;
    font-size: 14px;
    font-weight: 400;
    color: #333;
  }
  .vice-name{
    margin: 0 10px 10px;
    height: 18px;
    font-size: 12px;
    color: #b0b0b0;
    text-align: center;
    text-overflow: ellipsis;
    white-space: nowrap;
    overflow: hidden;
  }
  .price{
    display: block;
    margin: 0 10px 10px;
    text-align: center;
    .selling-price{
      color: #ff6700;
      display: inline-block;
    }
    .original-price{
      display: inline-block;
        margin-left: 0.5em;
      color: #b0b0b0;
      text-decoration: line-through;
    }
  }
}
</style>