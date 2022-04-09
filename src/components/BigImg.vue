<template>
<div class="big-img">
  <Card>
    <img src="https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/ac5cafc68c10ce4471869d378f594b52.png?thumb=1&w=293&h=768&f=webp&q=90" alt="">
  </Card>
</div>
</template>

<script>
import Card from "./Card.vue";
export default {
  name: "BigImg",
  components: {Card}
}
</script>

<style scoped>
.big-img img{
  display: block;
  width: 100%;
}
</style>