<template>
<div class="common-more">
  <Card class="common">
    <a :href="commonInformation.link" class="common-text">
      <div class="info">
        <h6 class="name">{{commonInformation.name}}</h6>
        <p class="price">{{commonInformation.sellingPrice}}</p>
      </div>
      <div class="img-box">
        <img :src="commonInformation.imgUrl" alt="">
      </div>
    </a>
  </Card>
  <Card>
    <a href="#" class="more">
      <div class="more-text">
        <h6>浏览更多</h6>
        <p>热门</p>
      </div>
      <div class="icon-box">
        <span class="iconfont icon-quanquanxiangyoujiantou"></span>
      </div>
    </a>
  </Card>
</div>
</template>

<script>
import Card from "./Card.vue";

export default {
  name: "CommonMore",
  components: {
    'Card': Card,
  },
  props:{
    commonInformation: Object,
  }
}
</script>

<style scoped lang="less">
  .common-more{
    .common{
      margin-bottom: 14px;
      .common-text{
        display: flex;
        align-items: center;
        height: 143px;
        //padding-top: 50px;
        padding-left: 30px;
        box-sizing: content-box;
        .info{
          width: 94px;
          .name{
            font-size: 14px;
            font-weight: 400;
            margin-bottom: 5px;
            color: #333;
          }
          .price{
            color: #ff6700;
          }
        }
        .img-box{
          margin-right: 20px;
          img{
            display: block;
            width: 80px;
            height: 80px;
          }
        }
      }
    }

    .more{
      height: 143px;
      padding: 0 30px;
      display: flex;
      align-items: center;
      justify-content: space-between;
      .more-text{
        h6{
          font-size: 18px;
          color: #333;
        }
        p{
          font-size: 12px;
          color: #757575;
        }
      }
      .icon-box{
        font-size: 44px;
        color: #ff6700;
      }
    }
  }

</style>