<script setup>
import Header from './Header.vue'
import Nav from './Nav.vue'
import Footer from './Footer.vue'
import Menu from './Menu.vue'
import MenuBanner from './MenuBanner.vue'
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
      <div class="sub">
        <div class="container">服务</div>
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
  height: 170px;
}
</style>