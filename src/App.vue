<template>
  <div class="wrap">
    <HeaderBanner/>
    <Header />
    <HeaderMenu />
  </div>
</template>

<script>
import HeaderBanner from './components/HeaderBanner.vue';
import Header  from './components/Header.vue'
import HeaderMenu from './components/HeaderMenu.vue';

export default {
  name: "App",
  components: { 
    HeaderBanner,
    Header,
    HeaderMenu
  },
};
</script>

<style>
  .commLayout{
    display: block;
    max-width: 1200px;
    width: 100%;
    margin: 0 auto;
  }
</style>