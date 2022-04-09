<template>
  <div class="sub container">
    <div class="sub-left">
      <ul>
        <li v-for="(sub, i) in subs" :key="i">
          <a href="#">
            <span :class="['iconfont', sub.icon, 'icon']"></span>
            <p>{{sub.text}}</p>
          </a>
        </li>
      </ul>
    </div>
    <div class="sub-right">
      <ul>
        <li style="margin-left: 0">
          <a href="#">
            <img src="../../assets/image/sub1.jpg" alt="">
          </a>
        </li>
        <li>
          <a href="#">
            <img src="../../assets/image/sub2.jpg" alt="">
          </a>
        </li>
        <li>
          <a href="#">
            <img src="../../assets/image/sub3.jpg" alt="">
          </a>
        </li>
      </ul>
    </div>
  </div>
</template>

<script setup>
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

<style scoped>
.sub {
  display: flex;
  height: 170px;
  margin-top: 14px;
  margin-bottom: 26px;
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
.sub-left a .icon{
  font-size: 16px;
  margin-bottom: 4px;
  display: block;
}
.sub-left li::before{
  content: '';
  width: 64px;
  height: 1px;
  background-color: #665e57;
  position: absolute;
  left: 6px;
  top: -1px;
}
.sub-left li::after{
  content: '';
  width: 1px;
  height: 64px;
  background-color: #665e57;
  position: absolute;
  left: -1px;
  top: 6px;
}
.sub-left li:nth-child(1)::before,
.sub-left li:nth-child(2)::before,
.sub-left li:nth-child(3)::before
{
  content: none;
}
.sub-left li:nth-child(1)::after,
.sub-left li:nth-child(4)::after{
  content: none;
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
.sub-right img{
  display: block;
  width: 100%;
}
</style>