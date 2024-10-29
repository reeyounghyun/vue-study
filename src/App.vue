<template>
  <div id="app" class="wrap">
    <Header />
  </div>
</template>

<script>
import Header  from './components/Header.vue'

export default {
  name: "App",
  components: { 
    Header
  },
};
</script>

<style>
  *{
    margin: 0;
    padding: 0;
  }
  img{
    max-width: 100%;
    width: auto;
    border: 0;
    border-style: none;
    vertical-align:middle;
  }
</style>