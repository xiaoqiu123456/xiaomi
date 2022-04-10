<template>
<div class="big-img">
  <Card>
    <img :src="src" alt="">
  </Card>
</div>
</template>

<script>
import Card from "./Card.vue";
export default {
  name: "BigImg",
  components: {Card},
  props:{
    src:String,
  }
}
</script>

<style scoped>
.big-img img{
  display: block;
  width: 100%;
}
</style>