<script setup>
import {ref} from "vue";

const lists = ref([
  {
    icon: 'icon-weixiu',
    name: '预约维修服务',
    links: '#'
  }, {
    icon: 'icon-7',
    name: '7天无理由退货',
    links: '#'
  }, {
    icon: 'icon-15',
    name: '15天无理由换货',
    links: '#'
  }, {
    icon: 'icon-liwu',
    name: '满69元包邮',
    links: '#'
  }, {
    icon: 'icon-weixiu',
    name: '预约维修服务',
    links: '#'
  }, {
    icon: 'icon-dingxiang',
    name: '520余家售后网点',
    links: '#'
  },
])

// ref { value }
const helpCenter = ref([
  {
    links: '#',
    name: '账户管理',
  },
  {
    links: '#',
    name: '购物指南',
  },
  {
    links: '#',
    name: '订单操作',
  },
])
const serviceSupport = ref([
  {
    links: '#',
    name: '售后政策',
  },
  {
    links: '#',
    name: '自助服务',
  },
  {
    links: '#',
    name: '相关下载',
  },
])
const offlineStores = ref([
  {
    links: '#',
    name: '小米之家',
  },
  {
    links: '#',
    name: '服务网点',
  },
  {
    links: '#',
    name: '授权体验店/专区',
  },
])
const aboutXiaom = ref([
  {
    links: '#',
    name: '了解小米',
  },
  {
    links: '#',
    name: '加入小米',
  },
  {
    links: '#',
    name: '投资者关系',
  },
  {
    links: '#',
    name: '企业社会责任',
  },
  {
    links: '#',
    name: '廉洁举报',
  },
])
const attention = ref([
  {
    links: '#',
    name: '新浪微博',
  },
  {
    links: '#',
    name: '官方微信',
  },
  {
    links: '#',
    name: '联系我们',
  },{
    links: '#',
    name: '公益基金会',
  },
])
const specialService = ref([
  {
    links: '#',
    name: 'F 码通道',
  },
  {
    links: '#',
    name: '礼物码',
  },
  {
    links: '#',
    name: '防伪查询',
  },
])

const linkList = [
  {
    title: '帮助中心',
    lists: helpCenter.value,
  },{
    title: '服务支持',
    lists: serviceSupport.value,
  },{
    title: '线下门店',
    lists: offlineStores.value,
  },{
    title: '关于小米',
    lists: aboutXiaom.value,
  },{
    title: '关注我们',
    lists: attention.value,
  },{
    title: '特色服务',
    lists: specialService.value,
  },
]
</script>

<template>
  <footer class="footer-box">
    <div class="container">
      <div class="footer-top">
        <ul>
          <li v-for="item in lists">
            <a :href="item.links">
              <span :class="{iconfont:true, [item.icon]: true}"></span>
              <p>{{ item.name }}</p>
            </a>
          </li>
        </ul>
      </div>
      <div class="footer-centent">
        <div class="links-box">
          <div class="link-items" v-for="item in linkList">
            <h3>{{item.title}}</h3>
            <ul>
              <li v-for="link in item.lists">
                <a>{{link.name}}</a>
              </li>
            </ul>
          </div>
        </div>
        <div class="contact">
            <h3>400-100-5678</h3>
            <p class="time">8:00-18:00（仅收市话费）</p>
            <a href="#">
              <span class="iconfont icon-duanxin"></span>
              <p>人工服务</p>
            </a>
            <p class="xiaomi">
              关注小米：
              <span class="iconfont icon-weibo"></span>
              <span class="iconfont icon-weixin">
                <img class="wx-code" src="https://cdn.cnbj1.fds.api.mi-img.com/staticsfile/global/wx-img.png" alt="">
              </span>
            </p>
        </div>
      </div>
    </div>
  </footer>
</template>

<style scoped lang="less">
.footer-box {
  //height: 600px;
  background-color: white;

  .footer-top {
    padding: 27px 0;
    border-bottom: 1px solid #e0e0e0;

    ul {
      display: flex;

      li {
        flex: 1;

        a {
          display: flex;
          font-size: 16px;
          line-height: 25px;
          justify-content: center;
          align-items: center;
          color: #616161;
          position: relative;

          &::after {
            content: '';
            width: 1px;
            height: 25px;
            background-color: #e0e0e0;
            position: absolute;
            right: 0;
            top: 0;
          }

          &:hover {
            color: #ff6700;
            transition: color 0.2s ease-in-out;
          }

          span {
            font-size: 24px;
            margin-right: 6px;
          }
        }

        &:last-child a::after {
          content: none;
        }
      }
    }
  }
  .footer-centent{
    display: flex;
    padding: 40px 0;
    .links-box{
      display: flex;
      .link-items{
        width: 160px;
        h3{
          margin: -1px 0 26px;
          font-size: 14px;
          color: #424242;
          font-weight: normal;
        }
        a{
          margin: 10px 0 0;
          font-size: 12px;
          color: #757575;
          &:hover{
            color: #ff6700;
            cursor: pointer;
            transition: color 0.3s;
          }
        }
      }
    }

    .contact{
      position: relative;
      align-self: start;
      flex: 1;
      display: flex;
      flex-direction: column;
      align-items: center;
      h3{
        color: #ff6700;
        font-size: 22px;
        margin-bottom: 5px;
      }
      .time{
        margin-bottom: 5px;
        font-size: 12px;
      }
      a{
        display: flex;
        justify-content: center;
        align-items: center;
        width: 120px;
        height: 30px;
        background-color: white;
        border: 1px solid #ff6700;
        font-size: 12px;
        color: #ff6700;
        transition: all 0.3s ease-in-out;
        .iconfont{
          margin-right: 2px;
        }
        &:hover{
          background-color: #ff6700;
          color: white;
        }
      }
      .xiaomi{
        font-size: 12px;
        margin-top: 10px;
        height: 21px;
        span{
          font-size: 20px;
          margin-left: 6px;
          line-height: 21px;
          transition: color .3s;
          &:hover{
            color: #ff6700;
          }
        }
        span.icon-weixin{
          position: relative;
          cursor: pointer;
          .wx-code{
            //display: none;
            opacity: 0;
            width: 126px;
            height: 126px;
            position: absolute;
            left: -60px;
            top: 24px;
            background-color: #e0e0e0;
            transition: opacity .3s ease-in-out;
          }
          &:hover .wx-code{
            //display: block;
            opacity: 1;
          }
        }
      }
      &::before{
        content: '';
        width: 1px;
        height: 100%;
        background-color: #e0e0e0;
        position: absolute;
        left: 0;
        top: 0;
      }
    }
  }
}
</style>