<template>
  <div class="video">
    <div class="video-title">
      <CommonTitle title="视频" more="查看更多"/>
    </div>
    <div class="video-box">
      <ul>
        <Card class="my-card"  v-for="item in videoList">
          <a :href="item.links" class="links">
            <div class="figure-img">
              <img :src="item.imgurl" alt="">
              <a class="btn">
                <span class="iconfont icon-gengduo"></span>
              </a>
            </div>
            <h3>{{ item.title }}</h3>
            <p>{{item.text}}</p>
          </a>
        </Card>
      </ul>
    </div>
  </div>
</template>

<script>
import CommonTitle from "./CommonTitle.vue";
import Card from "./Card.vue";
export default {
  name: "video",
  components: {CommonTitle, Card},
  data(){
    return {
      videoList: [
        {
          title:'2021年春季新品发布会第一场',
          imgurl:'https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/e74c4ff741bcdfc5b28a48a43e4edc6d.jpg?thumb=1&w=370&h=225&f=webp&q=90',
          text:'',
          links:'#'
        },
        {
          title:'Redmi 10X系列发布会',
          imgurl:'https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/101b19aca4bb489bcef0f503e44ec866.jpg?thumb=1&w=370&h=225&f=webp&q=90',
          text:'Redmi 10X系列发布会',
          links:'#'
        },
        {
          title:'小米10 青春版 发布会',
          imgurl:'https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/96563e75833ba4563bd469dd28203b09.jpg?thumb=1&w=370&h=225&f=webp&q=90',
          text:'',
          links:'#'
        },
        {
          title:'小米10 8K手机拍大片',
          imgurl:'https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/2fd26bb99b723337a2f8eaba84f7d5bb.jpg?thumb=1&w=370&h=225&f=webp&q=90',
          text:'',
          links:'#'
        },
      ]
    }
  }

}
</script>

<style scoped lang="less">
.video{

  .video-box{
    ul{
      display: flex;
      .my-card{
        flex-grow: 1;
        //width: 296px;
        height: 285px;
        background-color: white;
        margin-left: 14px;
        margin-bottom: 14px;
        .links{
          width: 100%;
          .figure-img{
            position: relative;
            &:hover{
              .btn{
                background-color: #ff6700;
                border-color: #ff6700;
              }
            }
            img{
              display: block;
              width: 100%;
              height: 180px;
            }
            margin-bottom: 28px;
            background-color: #ff6700;
          }
          h3{
            text-align: center;
            margin: 0 14px 6px;
            font-size: 14px;
            color: #333;
            font-weight: 400;
          }
          p{
            margin: 0 14px;
            height: 18px;
            font-size: 12px;
            color: #b0b0b0;
            text-align: center;
          }
          .btn{
            position: absolute;
            left: 20px;
            top: 144px;
            border: 2px solid #ffffff;
            width: 32px;
            height: 20px;
            box-sizing: content-box;
            border-radius: 12px;
            background-color: rgba(0,0,0,0.6);
            font-size: 14px;
            color: white;
            display: flex;
            justify-content: center;
            align-items: center;
            font-weight: bold;
            transition: background-color 0.2s ease-in-out, border-color 0.2s ease-in-out;
          }
        }
        &:first-child{
          margin-left: 0;
        }
      }
    }
  }
}
</style>