<template>
<div class="card">
<img :src="data.img" alt="">
<h1>{{data.title}}</h1>
</div>
</template>

<script>
// 往外傳
export default {
  // 接收
  props: {
    data: Object
  }
}
</script>
