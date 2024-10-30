<template>
  <div class="home">
    <SectionComponent title="2023 새해 여행을 위해, 우리 여행 갈까" :items="section1Items">
    </SectionComponent>
    <SectionComponent title="고객님을 위한 추천여행" :items="section2Items" />
  </div>
</template>

<script>
  import SectionComponent from './SectionComponent.vue'; //공통 색션 컴포넌트 불러옴.

  export default{
    components: {
      SectionComponent,
    },
    data() {
      return {
        section1Items: [
          { image: '/images/best_travel01.jpg', title: '상품1', description: '상품 설명', price: '1,388,700원' },
          { image: '/images/best_travel02.jpg', title: '상품2', description: '상품 설명', price: '779,000원' },
          { image: '/images/best_travel03.jpg', title: '상품2', description: '상품 설명', price: '779,000원' },
          { image: '/images/best_travel04.jpg', title: '상품2', description: '상품 설명', price: '779,000원' },
        ],
        // 두 번째 섹션에 필요한 여행 상품 리스트
        section2Items: [
          { image: '/images/best_travel01.jpg', title: '상품1', description: '상품 설명', price: '1,388,700원' },
          { image: '/images/best_travel02.jpg', title: '상품2', description: '상품 설명', price: '779,000원' },
          { image: '/images/best_travel03.jpg', title: '상품2', description: '상품 설명', price: '779,000원' },
          { image: '/images/best_travel04.jpg', title: '상품2', description: '상품 설명', price: '779,000원' },
        ],
      }
    },
  }
</script>

<style>

</style>