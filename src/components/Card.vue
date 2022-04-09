<template>
  <div class="card">
    <slot/>
  </div>
</template>

<script>
export default {
  name: "Card"
}
</script>

<style scoped>
.card{
  position: relative;
  z-index: 1;
  /*float: left;*/
  width: 234px;
  /*margin-left: 14px;*/
  /*margin-bottom: 14px;*/
  background: #fff;
  -webkit-transition: all .2s linear;
  transition: all .2s linear;
}
.card:hover {
  z-index: 2;
  -webkit-box-shadow: 0 15px 30px rgba(0,0,0,.1);
  box-shadow: 0 15px 30px rgba(0,0,0,.1);
  -webkit-transform: translate3d(0,-2px,0);
  transform: translate3d(0,-2px,0);
}
</style>