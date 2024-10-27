<template>
  <div class="nav">
    <a v-for="headerNav in nav" :key="headerNav">{{headerNav}}</a>
  </div>

  <!--
    <div v-for="(room,i) in 3" :key="room">
    <h4>{{products[i]}} 원룸</h4>
    <span>{{price1}} 만원</span>
  </div>
  -->
  <!-- 방법1 -->

  <!--
    <div v-for="(room,i) in products" :key="room">
    <h4>{{products[i]}} 원룸</h4>
    <span>{{price1}} 만원</span>
  </div>
  -->
  <!-- 방법2 -->

  <div>
    <h4>{{products[0]}}</h4>
    <p>10 만원</p>
    <button @click="lengthBtn[0]++">허위매물신고</button>
    <span>신고수 : {{ lengthBtn[0] }}</span>
  </div>

  <div>
    <h4>{{products[1]}}</h4>
    <p>10 만원</p>
    <button @click="lengthBtn[1]++">허위매물신고</button>
    <span>신고수 : {{ lengthBtn[1] }}</span>
  </div>

  <div>
    <h4>{{products[2]}}</h4>
    <p>10 만원</p>
    <button @click="lengthBtn[2]++">허위매물신고</button>
    <span>신고수 : {{ lengthBtn[2] }}</span>
  </div>
</template> 

<script>

export default {
  name: 'App',
  data(){
    return{
      lengthBtn:[0,0,0],
      price1: 60,
      price2: 30,
      price3: 100,
      products:['홍대원롬','신촌원롬','마포구원룸'],
      nav:['Home','products','About']
    }
  },
  components: {
  }
}
</script>

<style>
  .nav{
    background-color: blue;
    height: 30px;
    padding: 15px;
    color: #fff;
  }
  .nav a{
    font-size: 18px;
    padding: 15px;
  }
  #app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
  }
</style>
