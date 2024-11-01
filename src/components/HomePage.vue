<template>
  <div class="home">
    <SectionComponent title="2023 새해 여행을 위해, 우리 여행 갈까" :items="section1Items" class="section1Items">
    </SectionComponent>
    <TebSectionComponent tabText="이 겨울에 놓칠 수 없는 특별한 여행 혜택을 만나보세요!" :items="specialItems"/>
    <SectionComponent title="하나국제여행제 한정특가 2주차" subtitle="우주 수상상품과 함께 보는 초청여행지_시드니" :items="section2Items" class="section2Items"/>
  </div>
</template>

<script>
  import TebSectionComponent from './TebSectionComponent.vue';
  import SectionComponent from './SectionComponent.vue'; //공통 색션 컴포넌트 불러옴.

  export default{
    components: {
      TebSectionComponent,
      SectionComponent,
    },
    data() {
      return {
        section1Items: [
          { image: '/images/best_travel01.jpg', title: '훗카이도 4일', description: '#인기 온천호텔 #미식여행 #핵심관광', price: '1,388,700원~' },
          { image: '/images/best_travel02.jpg', title: '코타키나발루 5~6일', description: '#아일랜드투어 #반딧불투어', price: '779,000원' },
          { image: '/images/best_travel03.jpg', title: '하노이/하롱베이 5~6일', description: '#실속있게 #핵심관광', price: '459,900원' },
          { image: '/images/best_travel04.jpg', title: '이탈리아 일주 8,9일', description: '로마 벤츠 밴투어 #베네치아 대운하 투어', price: '2,690,000원' },
        ],
        // 두 번째 섹션에 필요한 여행 상품 리스트
        section2Items: [
          { image: '/images/best_travel01.jpg', title: '[하나국제여행제] 코타키나발루 5일', description: '선셋이 아름다움', price: '1,388,700원' },
          { image: '/images/best_travel02.jpg', title: '[하나국제여행제] 사이판 자유여행 4~5일', description: '익사이팅 사이판', price: '779,000원' },
          { image: '/images/best_travel03.jpg', title: '[하나국제여행제] 동유럽 3,4국 9일', description: '프라하의 낭만 야경', price: '779,000원' },
          { image: '/images/best_travel04.jpg', title: '[하나국제여행제] 호주/뉴질랜드 남북섬', description: '호주+뉴질랜드완전일주', price: '779,000원' },
        ],
      }
    },
  }
</script>

<style>
  .section1Items{
    padding-top: 100px;
  }
  .section2Items{
    padding-top: 50px;
  }
</style>