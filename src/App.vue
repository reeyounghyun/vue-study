<template>
  <div id="app" class="wrap">
    <Header />
    <HeaderMenu />
  </div>
</template>

<script>
import Header  from './components/Header.vue'
import HeaderMenu from './components/HeaderMenu.vue';

export default {
  name: "App",
  components: { 
    Header,
    HeaderMenu
  },
};
</script>

<style>
  .commLaout{
    display: block;
    max-width: 1200px;
    width: 100%;
    margin: 0 auto;
  }
</style>