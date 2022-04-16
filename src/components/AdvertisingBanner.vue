<template>
  <div class="advertising-banner">
    <a :href="links">
      <img
          :src="src"
          alt="">
    </a>
  </div>
</template>

<script>
// https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/0e2b43800d3e1ef40470ac04b3e0140b.jpg?thumb=1&w=1533&h=150&f=webp&q=90
export default {
  name: "AdvertisingBanner",
  props:{
    src: {
      type:String,
      default:null,
      required:true,
    },
    links:{
      type:String,
      default: '#',
      required: false,
    },
  }
}
</script>

<style scoped lang="less">
.advertising-banner {
  img {
    display: block;
    width: 100%;
    margin: 22px 0;
  }
}
</style>