<script setup>
import Header from './Header.vue'
import Nav from './Nav.vue'
import Footer from './Footer.vue'
import Menu from './Menu.vue'
import MenuBanner from './MenuBanner.vue'
const subs = [
  {
    icon: 'icon-naozhong',
    text: '保障服务'
  },{
    icon: 'icon-fangdichanjianzhu',
    text: '企业团购'
  },{
    icon: 'icon-fmabeifen2',
    text: 'F码通道'
  },{
    icon: 'icon-cunchuneicunka',
    text: '米粉卡'
  },{
    icon: 'icon-qian',
    text: '以旧换新'
  },{
    icon: 'icon-huafeichongzhi',
    text: '花费充值'
  },
]
</script>

<template>
  <div class="home-page">
    <Header></Header>
    <Nav></Nav>
    <main>
      <div class="menu-banner-wrap container">
        <div class="menu">
          <Menu/>
        </div>
        <div class="banner">
          <menu-banner></menu-banner>
        </div>
      </div>

      <!-- 服务 -->
      <div class="sub container">
        <div class="sub-left">
          <ul>
            <li v-for="(sub, i) in subs" :key="i">
              <a href="#">
                <span :class="['iconfont', sub.icon]"></span>
                <p>{{sub.text}}</p>
              </a>
            </li>
          </ul>
        </div>
        <div class="sub-right">
          <ul>
              <li style="margin-left: 0">
                <a href="#">
                  <img src="#" alt="">
                </a>
              </li>
            <li>
              <a href="#">
                <img src="#" alt="">
              </a>
            </li>
            <li>
              <a href="#">
                <img src="#" alt="">
              </a>
            </li>
          </ul>
        </div>
      </div>
    </main>

  </div>
</template>

<style>

.home-page {
  color: red;
}

.menu-banner-wrap {
  /*display: flex;*/
  position: relative;

}

.menu {
  height: 460px;
  position: absolute;
  left: 0;
  top: 0;
  z-index: 11;
  /*flex-shrink: 0;*/
}

.banner {
  /*width: 992px;*/
  background-color: antiquewhite;
}

.sub {
  display: flex;
  height: 170px;
  margin-top: 14px;
}
.sub-left{
  width: 234px;
  height: 170px;
}
.sub-left ul{
  margin: 0;
  padding: 3px;
  list-style-type: none;
  font-size: 12px;
  text-align: center;
  background: #5f5750;
  overflow: hidden;
}
.sub-left ul li{
  position: relative;
  float: left;
  width: 76px;
  height: 82px;
  padding: 0 3px;
}
.sub-left a{
  display: block;
  padding-top: 18px;
  text-overflow: ellipsis;
  color: #fff;
  opacity: .7;
  -webkit-transition: opacity .2s;
  transition: opacity .2s;
}
.sub-right{
  width: 978px;
  height: 170px;
  margin-left: 14px;
}
.sub-right ul{
  display: flex;
}
.sub-right li{
  width: 316px;
  height: 170px;
  margin-left: 15px;
  background-color: #007aff;
}
</style>