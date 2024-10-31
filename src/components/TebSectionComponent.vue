<template>
  <div class="section2Items">
    <div class="tabSection commLayout">
      <div class="tabCont">
        <div class="backgroung-image">
          <h2>마침내 특가 <br/> 추운 겨울에도  <br/>여행 텐션 UP!</h2>
          <div class="tab-buttons">
            <button
              v-for="(tab, index) in tabs"
              :key="index"
              :class="{ active: activeTab === index }"
              @click="setActiveTab(index)" 
            >
              {{ tab }}
            </button>
          </div>
          <div v-if="activeTab === 0" class="tab-content"></div>
          <div v-if="activeTab === 1" class="tab-content"></div>
          <div v-if="activeTab === 2" class="tab-content"></div>
          <div v-if="activeTab === 3" class="tab-content"></div>
        </div>
        <div class="tabList">
          <div v-for="(item, index) in filteredItems" :key="index" class="card-item">
            <img :src="item.image" :alt="item.title" />
            <div class="textBox">
              <span class="subTitle">{{ item.subtTitle }}</span>
              <h3 class="tabTitle">{{ item.title }}</h3>
              <p class="tavdec">{{ item.description }}</p>
              <span class="tabPro">{{ item.prodect }}</span>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        activeTab: 0,
        tabs: [
          "여유있는 발걸음 일본",
          "내가 찾는 힐링 동남아",
          "겨울 동화 속으로 유럽",
          "따스한 햇살, 남태평양",
        ],
        // 각 탭에 맞는 아이템 리스트 정의
        itemsTab1: [
          { image: '/images/tab_bg01.jpg', subtTitle: '에어텔', title: '규슈 3,4일 #자유여행 #시내숙박', description: '일본 상품 설명 1', prodect: '100,000~' },
          { image: '/images/tab_bg01.jpg', subtTitle: '에어텔', title: '일본 상품 2', description: '일본 상품 설명 2', prodect: '100,000~' },
          { image: '/images/tab_bg01.jpg', subtTitle: '에어텔', title: '일본 상품 2', description: '일본 상품 설명 2', prodect: '100,000~' },
        ],
        itemsTab2: [
          { image: '/images/tab_bg01.jpg', subtTitle: '에어텔', title: '일본 상품 2', description: '일본 상품 설명 2', prodect: '100,000~' },
          { image: '/images/tab_bg01.jpg', subtTitle: '에어텔', title: '규슈 3,4일 #자유여행 #시내숙박', description: '일본 상품 설명 1', prodect: '100,000~' },
          { image: '/images/tab_bg01.jpg', subtTitle: '에어텔', title: '일본 상품 2', description: '일본 상품 설명 2', prodect: '100,000~' },
        ],
        itemsTab3: [
          { image: '/images/tab_bg01.jpg', subtTitle: '에어텔', title: '일본 상품 2', description: '일본 상품 설명 2', prodect: '100,000~' },
          { image: '/images/tab_bg01.jpg', subtTitle: '에어텔', title: '일본 상품 2', description: '일본 상품 설명 2', prodect: '100,000~' },
          { image: '/images/tab_bg01.jpg', subtTitle: '에어텔', title: '규슈 3,4일 #자유여행 #시내숙박', description: '일본 상품 설명 1', prodect: '100,000~' },
        ],
        itemsTab4: [
          { image: '/images/tab_bg01.jpg', subtTitle: '에어텔', title: '일본 상품 2', description: '일본 상품 설명 2', prodect: '100,000~' },
          { image: '/images/tab_bg01.jpg', subtTitle: '에어텔', title: '규슈 3,4일 #자유여행 #시내숙박', description: '일본 상품 설명 1', prodect: '100,000~' },
          { image: '/images/tab_bg01.jpg', subtTitle: '에어텔', title: '일본 상품 2', description: '일본 상품 설명 2', prodect: '100,000~' },
        ],
      };
    },
    computed: {
      // activeTab 값에 따라 적절한 아이템 리스트를 반환
      filteredItems() {
        switch (this.activeTab) {
          case 0:
            return this.itemsTab1;
          case 1:
            return this.itemsTab2;
          case 2:
            return this.itemsTab3;
          case 3:
            return this.itemsTab4;
          default:
            return [];
        }
      },
    },
    methods: {
      setActiveTab(index) {
        this.activeTab = index;
      },
    },
  };
</script>

<style scoped>
  .tabSection {
    display: flex;
    flex-direction: column;
  }
  .tabSection .tabCont{
    position: relative;
    display:flex;
    align-items: flex-start;
  }
  .tabSection .backgroung-image{
    padding: 50px 50px;
  }
  .tabSection .backgroung-image h2{
    display: block;
    font-size: 39px;
    line-height: 48px;
    color: #fff;
  }
  .tabSection .tab-buttons {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    gap: 10px;
    margin-top: 41px;
  }
  .tabSection .tab-buttons button{
    display: block;
    width: 200px;
    font-size: 13px;
    font-weight: 400;
    border-radius: 20px;
    padding: 10px 20px;
  }
  .backgroung-image{
    background: url(/images/inner_bg.jpg) no-repeat;
    width: 434px;
    height: 566px;
    display: inline-block;
    padding-left: 60px;
    background-size: contain;
    background-position: left center;
  }
  button {
    padding: 10px;
    border: none;
    border-radius: 5px;
    cursor: pointer;
  }
  button.active {
    background-color: #333;
    color: #fff;
  }
  .tab-content {
    margin-top: 20px;
  }
  .tabList {
    position: absolute;
    right: 0;
    top: 0;
    display: flex;
    gap: 10px;
    margin-top: 55px;
  }
  .tabList .card-item {
    max-width: 282px;
    background-color: #fff;
    box-shadow: 3px 5px 10px #ededed;
    box-sizing: border-box;
    border-radius: 5px;
  }
  .card-item .card-item img{
    height: 210px;
  }
  .tabList .textBox{
    display: block;
    padding: 10px 15px;
    height: 210px;
  }
  .tabList .subTitle{
    display: block;
    padding-bottom: 12px;
    font-size: 13px;
    color: #575757;
    text-align: left;
  }
  .tabList .tabTitle{
    display: block;
    padding-bottom: 10px;
    font-size: 20px;
    font-weight: 600;
    color: #000;
  }
  .tabList .tavdec{
    font-size: 13px;
    color: #000;
    padding-bottom: 12px;
  }
  .tabList .tabPro{
    font-size: 24px;
    font-weight: 800;
    padding-bottom: 12px;
  }
</style>
