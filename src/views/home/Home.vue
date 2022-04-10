<script setup>
import Header from './Header.vue'
import Nav from './Nav.vue'
import Footer from './Footer.vue'
import Menu from './Menu.vue'
import MenuBanner from './MenuBanner.vue'
import Sub from "./Sub.vue";
import Phone from "./Phone.vue";



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
      <Sub/>

      <div style="background-color: #f5f5f5">
        <div class="container">

          <div class="advertising-banner">
            <a href="#">
              <img src="https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/0e2b43800d3e1ef40470ac04b3e0140b.jpg?thumb=1&w=1533&h=150&f=webp&q=90" alt="">
            </a>
          </div>

          <Phone/>
        </div>
      </div>
    </main>

  </div>
</template>

<style lang="less">

.home-page {
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
.advertising-banner{
  img{
    display: block;
    width: 100%;
    margin: 22px 0;
  }
}




</style>