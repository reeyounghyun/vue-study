<template>
  <div class="wrap">
    <HeaderBanner/>
    <Header></Header>
    <HeaderMenu />
    <HomePage/>
    <SnsMainComponent/>
    <Footer></Footer>
</div>
</template>

<script>
import HeaderBanner from './components/HeaderBanner.vue';
import Header  from './components/Header.vue'
import HeaderMenu from './components/HeaderMenu.vue';
import HomePage from './components/HomePage.vue'
import SnsMainComponent from './components/SnsMainComponent.vue'
import Footer from './components/Footer.vue';


export default {
  name: "App",
  components: { 
    HeaderBanner,
    Header,
    HeaderMenu,
    HomePage,
    SnsMainComponent,
    Footer,
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