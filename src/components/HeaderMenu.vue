<template>
  <nav class="nav">
    <div class="gnb">
      <div class="menuWrap commLayout">
        <div class="allMenu">
          <img src="/images/ico-allmenu.png" alt="전체 메뉴 아이콘">
          <span>전체메뉴</span>
        </div>
        <div class="hoverMenu">
          <div class="left">
            <ul>
              <li v-for="item in leftMenuItems" :key="item">
                <a href="#">
                  <span>{{item}}</span>
                </a>
              </li>
            </ul>
          </div>
          <div class="right">
            <ul>
              <li v-for="item in rightMenuItems" :key="item">
                <a href="#">
                  <span>{{ item }}</span>
                </a>
              </li>
            </ul>
          </div>
        </div>
      </div>
    </div>
  </nav>
</template>

<script>
  export default{
    data() {
      return {
          leftMenuItems: [
            "베스트",
            "해외여행",
            "항공",
            "호텔",
            "항공+호텔",
            "투어/입장권",
            "국내여행",
            "테마여행",
            "제우스",
            "하나LIVE",
        ],
        rightMenuItems: [
          "여행기획전",
          "이달의 혜택",
        ],
      }
    },
  }
</script>

<style scoped>
  .gnb{
    border-top: 1px solid #ddd;
  }
  .menuWrap {
    display: flex; 
    align-items: center; 
  }
  .menuWrap .allMenu{
    position: relative;
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 10px;
    max-width: 138px;
    width: 100%;
    height: 57px;
    line-height: 57px;
    border-left: 1px solid #ddd;
    border-right: 1px solid #ddd;
    font-size: 15px;
    color: #111;
    font-weight: 500;
  }
  .menuWrap .hoverMenu{
    display: flex; 
    align-items: center;
    justify-content: space-between;
    width: 100%; 
  }
  .menuWrap .hoverMenu ul{
    display: flex; 
    align-items: center; 
  }
  .menuWrap .hoverMenu ul li{
    line-height: 56px;
    height: 57px;
  }
  .menuWrap .hoverMenu ul li a{
    display: block;
  }
  .menuWrap .hoverMenu ul li a span{
    color: #111;
    font-size: 15px;
    font-weight: 500;
  }
  .menuWrap .hoverMenu .left ul li{
    padding-left: 25px;
  }
  .menuWrap .hoverMenu .right ul{
    gap: 10px;
  }
  .menuWrap .hoverMenu .right ul li + li{
    padding-left: 15px;
  }
</style>