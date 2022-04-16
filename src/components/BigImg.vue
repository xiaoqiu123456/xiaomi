<template>
  <div>
    <div class="big-img" v-if="typeof src === 'string'">
      <Card>
        <img :src="src" alt="">
      </Card>
    </div>
    <div v-else class="big-img-array">
      <Card v-for="item in src" :key="item">
        <img :src="item" alt="">
      </Card>
    </div>
  </div>
</template>

<script>
import Card from "./Card.vue";
export default {
  name: "BigImg",
  components: {Card},
  props:{
    src: [String, Array],
  }
}
</script>

<style scoped lang="less">
.big-img img{
}
.big-img-array{
  display: flex;
  flex-direction: column;
  & .card:first-child{
    margin-bottom: 14px;
  }
}
.big-img img,
.big-img-array img{
  display: block;
  width: 100%;
}
</style>