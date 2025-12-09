<template>
  <div class="wrap">
<!--    item: 배열 안에 들어 있는 객체 자체-->
<!--    index: 그 객체가 배열 안에서 몇 번째인지 알려주는 숫자-->
    <div class="items" v-for="(item, index) in moreItems" :key="index">
      <div class="image">이미지</div>
      <h5 :title="item.title">
        {{ item.title }}
      </h5>
    </div>
  </div>
</template>

<script>
  export default{
    data() {
      return {
        moreItems: [
          { title: '카드 뉴스 제목 01' },
          { title: '카드 뉴스 제목 02' }
        ]
      }

    }
  }
</script>

<style scoped>
</style>
