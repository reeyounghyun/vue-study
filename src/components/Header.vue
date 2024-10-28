<template>
  <header>
    <div class="myMenu">
      <ul>
        <li> 
          <a href="#" aria-label="로그인">
            <span>로그인</span>
          </a>
        </li>
        <li> 
          <a href="#" aria-label="회원가입">
            <span>회원가입</span>
          </a>
        </li>
        <li> 
          <a href="#" aria-label="고객센터 ">
            <span>고객센터</span>
          </a>
        </li>
      </ul>
    </div>


    <div class="headerInner">
      <div class="leftList">
        <h1>
          <img src="/images/header_logo.png" alt="하나투어" width="100" height="auto">
        </h1>
        <span class="search">검색창</span>
        <span class="search">실시간검색어</span>
      </div>
      <!-- <div class="myPageList">
        <div class="list">
          <img src="/images/ico-mymenu.png" alt="마이페이지" width="24" height="24">
          <p>마이메뉴</p>
        </div>
        <div class="list">
          <img src="/images/ico-reservationhistory.png" alt="예약내역" width="20" height="auto">
          <p>예약내역</p>
        </div>
        <div class="list">
          <img src="/images/ico-haeder-choice.png" alt="찜" width="24" height="auto">
          <p>찜</p>
        </div>
      </div> -->
      <div class="myPageList">
        <div class="list" v-for="(item, index) in myMenuItems" :key="index">
          <img :src="item.iconSrc" :alt="item.altText" :width="item.iconWidth" :height="item.iconHeight">
          <p>{{ item.title }}</p>
        </div>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  data() {
    return {
      myMenuItems: [
        { iconSrc: "/images/ico-mymenu.png", altText: "마이페이지", title: "마이메뉴", iconWidth: "24", iconHeight: "24" },
        { iconSrc: "/images/ico-reservationhistory.png", altText: "예약내역", title: "예약내역", iconWidth: "20", iconHeight: "auto" },
        { iconSrc: "/images/ico-haeder-choice.png", altText: "찜", title: "찜", iconWidth: "24", iconHeight: "auto" }
      ]
    };
  }
};
</script>

<style scoped>
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

#app {
  color: #333;
}
.myMenu{
  display: block;
  width: 100%;
  width: 1200px;
  max-width: 100%;
  margin: 0 auto;
  padding-bottom: 20px;
}
.myMenu ul{
  display: flex;
  align-items: center;
  justify-content: flex-end;
}
.myMenu ul li{
  list-style: none;
}
.myMenu ul li + li{
  padding-left: 20px;
}
.myMenu ul li a span{
  font-size: 12px;
  color: #000;
}
.headerInner{
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding-bottom: 20px;
  width: 1200px;
  max-width: 100%;
  margin: 0 auto;
}
.headerInner .leftList{
  display: flex;
  align-items: center;
}
.headerInner .leftList>h1{
  width: 150px;
}
.search{
  padding: 0 10px;
}
span{
  display: inline-block;
  font-size: 14px;
  color: #333;
}
.myPageList{
  display: flex;
  align-items: center;
  justify-content: flex-end;
}
.myPageList .list +.list{
  padding-left: 10px;
}
.myPageList .list{
  display: flex;
  align-items: center;
  flex-direction: column;
}
.myPageList .list p{
  display: blcok;
  margin-top: 3px;  
  font-size: 12px;
  font-weight: 400;
}
</style>
