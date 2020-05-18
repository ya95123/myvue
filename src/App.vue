<template>
  <div id="app">
    <h1>{{text}}</h1>
  </div>
</template>

<script>
// 要匯出去的資訊
export default {
  data () {
    return {
      text: 'aaa'
    }
  }
}
</script>

<style>
h1 {
  color: red
}
</style>
