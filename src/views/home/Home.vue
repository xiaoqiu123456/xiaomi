<script setup>
import Header from './Header.vue'
import Nav from './Nav.vue'
import Footer from './Footer.vue'
import Menu from './Menu.vue'
import MenuBanner from './MenuBanner.vue'
import Sub from "./Sub.vue";
import Phone from "./Phone.vue";
import Wear from "./Wear.vue";
import Notebook from "./Notebook.vue";
import ElectricAppliance from "./ElectricAppliance.vue";
import HouseholdAppliances from "./HouseholdAppliances.vue";
import AdvertisingBanner from "../../components/AdvertisingBanner.vue";
import KitchenAppliances from "./KitchenAppliances.vue";
import SmartHome from "./SmartHome.vue";
import SportsTravel from "./SportsTravel.vue";
import DailyNecessities from "./DailyNecessities.vue";
import Video from "../../components/Video.vue";



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

          <AdvertisingBanner src="https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/0e2b43800d3e1ef40470ac04b3e0140b.jpg?thumb=1&w=1533&h=150&f=webp&q=90" />

          <Phone/>

          <Wear/>
          <Notebook/>
          <ElectricAppliance/>
          <HouseholdAppliances/>
          <AdvertisingBanner src="https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/83c20664e83d8a6a8e938f2ba7e80e18.png?thumb=1&w=1533&h=150&f=webp&q=90"/>
          <KitchenAppliances/>
          <SmartHome/>
          <SportsTravel/>
          <AdvertisingBanner src="https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/88e35cffc82cd98cd53172460067af17.jpg?thumb=1&w=1533&h=150&f=webp&q=90"/>
          <DailyNecessities/>
          <Video/>
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





</style>