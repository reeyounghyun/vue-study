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
        <span class="search">
          <div class="wrap">
            <input class="search-input" type="search" placeholder="검색어를 입력해주세요" aria-label="검색어 입력란">
            <button class="search-button" aria-label="검색"></button>
          </div>
        </span>
        <span class="">실시간검색어</span>
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
    justify-content: center;
    gap: 20px;
    width: 100%;
    max-width: 800px;
  }
  .headerInner .leftList>h1{
    width: 150px;
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
  .search{
    position: relative;
    overflow: hidden;
    display: inline-block;
    width: 100%;
    max-width: 410px;
    height: 40px;
    border-radius: 100px;
    border: solid 2px #111;
  }
  .search .wrap{
    position: relative;
    width: 376px;
    display: flex;
    align-items: center;
    overflow: hidden;
    margin: 0 12px 0 20px;
    height: 40px;
  }
  .search .wrap .search-input{
    display: inline-block;
    max-width: 310px;
    width: 100%;
    padding: 8px 12px;
    flex: 1;
    outline: none;
    border: none;
    height: 40px;
    line-height: 40px;
    font-size: 15px;
    border-radius: 100px;
    color: #111;
  }
  .search .wrap input[type="search"]::-webkit-search-cancel-button {
      display: none;
  }
  .search .wrap .search-input:focus {
    width: 310px;
    margin-right: 24px;
    border: none !important;
  }

  .search .wrap .search-input::placeholder{
    font-size: 14px;
    color: #333;
    font-weight: 400;
  }
  .search .wrap .search-button{
    position: absolute;
    right: 15px;
    background: url(/images/ico-search.png) no-repeat;
    background-size: contain;
    width: 20px;
    height: 20px;
    background-position: center center;
    border: none;
    cursor: pointer;
  }
</style>
