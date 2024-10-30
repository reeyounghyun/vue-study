<template>
  <div class="headerBanner">
    <div class="inner">
      <div class="item" v-for="(item, index) in BannerItems" :key="index">
      <img :src="item.banSrc" :alt="item.altTeaxt" :width="item.banWidth" :height="item.banHeight">
    </div>
    </div>
  </div>
</template>

<script>
  export default{
    data() {
      return {
        BannerItems: [
          {banSrc: "/images/pc_top_2.jpg", altTeaxt: '배너1', banWidth:"599", banHeight:"90"},
          {banSrc: '/images/pc_top_2_42.jpg', altTeaxt: '배너2', banWidth:"599", banHeight:"90"},
        ]
      }
    },
  }
</script>

<style>
  .headerBanner{
    background-color: #fcf0f3;
  }
  .headerBanner .inner{
    display: flex;
    align-items: center;
    justify-content: center;
    max-width: 1200px;
    margin: 0 auto;
    width: 100%;
  }
  .headerBanner .inner .item{}
</style>