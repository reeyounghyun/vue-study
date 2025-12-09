<template>
<!--  <div class="wrap">-->
<!--    <HeaderBanner/>-->
<!--    <Header></Header>-->
<!--    <HeaderMenu />-->
<!--    <HomePage/>-->
<!--    <SnsMainComponent/>-->
<!--    <Footer></Footer>-->
<!--  </div>-->
  <div class="APP">
    <moerIndex />
  </div>
</template>

<script>
import moerIndex from './MoerCliek/moerIndex.vue';

// import HeaderBanner from './components/HeaderBanner.vue';
// import Header  from './components/Header.vue'
// import HeaderMenu from './components/HeaderMenu.vue';
// import HomePage from './components/HomePage.vue'
// import SnsMainComponent from './components/SnsMainComponent.vue'
// import Footer from './components/Footer.vue';

export default {
  name: "App",
  components: {
    moerIndex,
    // HeaderBanner,
    // Header,
    // HeaderMenu,
    // HomePage,
    // SnsMainComponent,
    // Footer,
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