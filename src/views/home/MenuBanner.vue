<template>
  <div class="swiper my-swiper">
    <div class="swiper-wrapper">
      <div class="swiper-slide" v-for="item in banners" :key="item.link">
        <a :href="item.link" target="_blank">
          <img :src="item.imgUrl"/>
        </a>
      </div>
    </div>
    <div class="swiper-button-next"></div>
    <div class="swiper-button-prev"></div>

    <div class="swiper-pagination"></div>
  </div>
</template>
<script>
import {onMounted, nextTick} from 'vue';
import banner1 from '../../assets/image/banner1.jpg'
import banner2 from '../../assets/image/banner2.jpg'
import banner3 from '../../assets/image/banner3.jpg'
import banner4 from '../../assets/image/banner.4.webp'
import banner5 from '../../assets/image/banner.5.webp'

export default {
  setup() {

    const banners = [
      {
        "imgUrl": banner1,
        "link": "https://www.mi.com/a/h/23479.html?sign=0efbd8867a728f56ab9999d7b33a45fb"
      }, {
        "imgUrl": banner2,
        "link": "https://www.mi.com/redmik50"
      }, {
        "imgUrl": banner3,
        "link": "https://www.mi.com/a/h/23654.html?sign=f094507ef59af38ee29f171c3ff7519c"
      }, {
        "imgUrl": banner4,
        "link": "https://m.mi.com/crowdfunding/proddetail/1000429"

      }, {
        "imgUrl": banner5,
        "link": "https://www.mi.com/buy?product_id=15820"
      }
      ]

    // 生命周期 - 挂载时执行
    onMounted(() => {
      const swiper = new Swiper(".my-swiper", {
        // 如果需要分页器
        loop: true,
        pagination: {
          el: '.swiper-pagination',
          clickable: true,
          renderBullet: function (index, className) {
            return `<span class="${className}"></span>`
            // return '<span class="' + className + '">' + (index + 1) + "</span>";
          },
        },
        navigation: {
          nextEl: ".swiper-button-next",
          prevEl: ".swiper-button-prev",
        },
      });
    })

    return {
      banners
    };
  },
};
</script>

<style>
.swiper {
  width: 100%;
  height: 100%;
}

.swiper-slide {
  text-align: center;
  font-size: 18px;
  /* background: #fff; */

  /* Center slide text vertically */
  display: -webkit-box;
  display: -ms-flexbox;
  display: -webkit-flex;
  display: flex;
  -webkit-box-pack: center;
  -ms-flex-pack: center;
  -webkit-justify-content: center;
  justify-content: center;
  -webkit-box-align: center;
  -ms-flex-align: center;
  -webkit-align-items: center;
  align-items: center;
}

.swiper-slide img {
  display: block;
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.my-swiper .swiper-pagination {
  width: 400px;
  left: auto;
  right: 30px;
  bottom: 20px;
  text-align: right;
}

.my-swiper .swiper-pagination .swiper-pagination-bullet {
  width: 6px;
  height: 6px;
  border: 2px solid #fff;
  border-color: hsla(0, 0%, 100%, .3);
  border-radius: 10px;
  overflow: hidden;
  background: rgba(0, 0, 0, .4);
  opacity: 1;
  box-sizing: content-box;
}

.my-swiper .swiper-pagination .swiper-pagination-bullet-active {
  background: hsla(0, 0%, 100%, .4);
  border-color: rgba(0, 0, 0, .4);
}

.my-swiper .swiper-button-next,
.my-swiper .swiper-button-prev {
  background: url('https://i1.mifile.cn/f/i/2014/cn/icon/icon-slides.png') no-repeat -125px 50%;
  right: 0;
  left: auto;
}

.my-swiper .swiper-button-prev {
  left: 234px;
  right: auto;
  background-position: -84px 50%;
}

.swiper-button-prev:hover, .swiper-container-rtl .swiper-button-next:hover {
  background-position: 0 50%;
}

.swiper-button-next:hover, .swiper-container-rtl .swiper-button-prev:hover {
  background-position: -42px 50%;
}

.my-swiper .swiper-button-next,
.my-swiper .swiper-button-prev {
  position: absolute;
  top: 50%;
  width: 41px;
  height: 69px;
  margin-top: -35px;
  z-index: 10;
  cursor: pointer;
  outline: none;
}

.swiper-button-next:after, .swiper-button-prev:after {
  content: '';
}
</style>