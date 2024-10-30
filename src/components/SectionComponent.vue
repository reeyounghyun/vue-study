<template>
  <div class="section commLayout">
    <h2>{{ title }}</h2>
    <div class="card-list">
      <div v-for="(item, index) in items" :key="index" class="card-item">
        <figure>
          <img :src="item.image" :alt="item.title">
        </figure>
        <h3>{{ item.title }}</h3>
        <p>{{ item.description }}</p>
        <p>{{ item.price }}</p>
      </div>
    </div>
  </div>
</template>

<script>
  export default{
    props: {
      title:String,
      items:Array,
    },
  }
</script>

<style>
.card-list{
  display: flex;
  align-items: center;
  justify-content: space-between;
}
.card-item figure{
  display: block;
  max-width: 250px;
}
.card-item img {
  display: block;
  width: 100%;
  height: 100%;
  margin: 0 auto;
  object-fit: cover;
}
</style>