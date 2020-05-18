<template>
  <div id="app">
    <h1>{{text}}</h1>
    <!-- 直接抓取 -->
    <!-- <Card :data="cards[0]"></Card> -->
    <!-- 在 cli 裡迴圈裡一定要加上 index 和 綁定 :key="index" -->
    <div class="cards">
      <Card class="card" v-for="(card,index) in cards" :key="index" :data="card"></Card>
      </div>
  </div>
</template>

<script>
// 1.引進 "元件名稱" from "路徑"
import Card from './components/Card.vue'
// 要匯出去的資訊
export default {
  data () {
    return {
      text: 'aaa',
      cards: [
        {
          img: 'https://picsum.photos/300/200/?random=1',
          title: '第1張卡片',
          goodNum: 0
        },
        {
          img: 'https://picsum.photos/300/200/?random=2',
          title: '第2張卡片',
          goodNum: 0

        }
      ]
    }
  },
  // 2.子元件
  components: {
    // 檔案名稱
    Card
  }
}
</script>

<style scoped lang="stylus">
// scoped 會只使用在這個元件裡
// h1
//   color red
</style>
