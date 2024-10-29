<template>
  <div class="commLaout">
    <div class="manuWrap">
      <div class="allMenu">전체메뉴</div>
      <div class="hoverMenu">
        <div class="left">
          <ul>
            <li class="leftItem"><a href="#"><span>베스트</span></a></li>
            <li><a href="#"><span>해외여행</span></a></li>
            <li><a href="#"><span>항공</span></a></li>
            <li><a href="#"><span>호텔</span></a></li>
            <li><a href="#"><span>항공+호텔</span></a></li>
            <li><a href="#"><span>투어/입장권</span></a></li>
            <li><a href="#"><span>국내여행</span></a></li>
            <li><a href="#"><span>태마여행</span></a></li>
            <li><a href="#"><span>제우스</span></a></li>
            <li><a href="#"><span>하나LIVE</span></a></li>
          </ul>
        </div>
        <div class="right">
          <ul>
            <li><a href="#"><span>여행기획전</span></a></li>
            <li><a href="#"><span>맞춤여행</span></a></li>
            <li><a href="#"><span>이당의 혜택</span></a></li>
          </ul>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
  export default{
    data() {
      return {
        
      }
    },
  }
</script>

<style scoped>
  .manuWrap{
    display: flex; 
    align-items: center; 
    border-top: 1px solid #ddd;
  }
  .manuWrap .allMenu{
    max-width: 138px;
    width: 100%;
    height: 57px;
    line-height: 57px;
    border: 1px solid #ddd;
    border-bottom: 1px solid #111;
    font-size: 15px;
    position: relative;
    padding-left: 57px;
    color: #111;
  }
  .manuWrap .hoverMenu{
    display: flex; 
    align-items: center;
    justify-content: space-between;
    width: 100%; 
    border-bottom: 1px solid #111;
  }
  .manuWrap .hoverMenu ul{
    display: flex; 
    align-items: center; 
  }
  .manuWrap .hoverMenu .left ul li{
    line-height: 56px;
    height: 57px;
  }
  .manuWrap .hoverMenu .left ul li.leftItem{
    padding-left: 25px;
  }
  .manuWrap .hoverMenu .left ul li + li{
    padding-left: 25px;
  }
  .manuWrap .hoverMenu ul li a span{
    color: #111;
    font-size: 15px;
  }

  .manuWrap .hoverMenu .right ul li + li{
    padding-left: 15;
  }
</style>