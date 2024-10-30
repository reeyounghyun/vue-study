<template>
  <div class="section commLayout">
    <h2>{{ title }}</h2>
    <p v-if="subtitle" class="subtitle">{{ subtitle }}</p>
    <div class="card-list">
      <div v-for="(item, index) in items" :key="index" class="card-item">
        <figure>
          <img :src="item.image" :alt="item.title">
        </figure>
        <div class="contInner">
          <h3>{{ item.title }}</h3>
          <p class="description">{{ item.description }}</p>
          <p class="price">{{ item.price }}</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
  export default{
    props: {
      title:String,
      subtitle: String,
      items:Array,
    },
  }
</script>

<style>
  .subtitle {
    color: #666; /* 서브타이틀 스타일 설정 */
    font-size: 14px;
    margin-top: -5px;
  }
  .section1Items h2{
    padding-bottom: 15px;
  }
  .section2Items h2{
    padding-bottom: 7px;
  }
  .section2Items p{
    padding-bottom: 15px;
  }
  .section .card-list{
    display: flex;
    align-items: center;
    justify-content: space-between;
  }
  .section .card-list .card-item {
    flex: 1 1 25%;
    width: 25%;
    margin: 7px;
  }
  .section .card-item figure{
    display: block;
    height: 210px;
  }
  .section .card-item img {
    display: block;
    width: 100%;
    height: 100%;
    margin: 0 auto;
    object-fit: cover;
  }
  .contInner{
    padding-top: 10px;
  }
  .contInner h3{
    font-size: 18px;
    font-weight: 600;
    margin-bottom: 8px;
    letter-spacing: -0.75px;
  }
  .contInner .description{
    font-size: 14px;
    font-weight: 400;
    margin-bottom: 3px;
    letter-spacing: -0.75px;
    color: #292929;
  }
  .contInner .price{
    font-size: 22px;
    font-weight: 700;
    letter-spacing: -0.75px;
  }
</style>