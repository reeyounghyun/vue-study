<template>
    <div class="berMenu">
        <ul>
            <li v-for="itme in footerList" :key="itme.id" >
                <a :href="itme.href">
                    <img :src="itme.src" :alt="itme.alt">
                    <span>{{ itme.title }}</span>
                </a>
            </li>
        </ul>
        <div class="infoWrap">
          <div class="inner">
            <div class="infoTitle">
              <h3>하나투어닷컴<br/>고객센터</h3>
              <strong>1577-1233</strong>
              <div class="link link1"><a href="#"><span>자주 찾는 질문</span></a></div>
              <div class="link"><a href="#"><span>ARS상담번호 안내</span></a></div>
            </div>
            <div class="infoTCenter">
              <div class="group1">
                <div class="comm-item item1">
                  <strong>해외여행 문의</strong>
                  <span>연중무휴:09:00~20:00</span>
                </div>
                <div class="comm-item item2">
                  <strong>해외항공권 문의</strong>
                  <span>1899-1833</span>
                  <span>평일:09:00~17:00</span>
                  <span>(점심시간:12:00~13:00)</span>
                </div>
              </div>
              <div class="group1">
                <div class="comm-item item3">
                  <strong>국내여행 문의</strong>
                  <span>평일/주말:09:00~20:00</span>
                </div>
                <div class="comm-item item4">
                  <strong>국내항공/국내숙박 문의</strong>
                  <span>평일:09:00~18:00</span>
                  <span>(점심시간:12:00~13:00)</span>
                  <span>주말:10:00~16:00</span>
                  <span>공휴일:10:00~14:00</span>
                  <p>*주말/공휴일은 긴급상담만 가능(업무처리 불가)</p>
                </div>
                <div class="comm-item item5">
                  <strong>기업출장/ 교육여행 단체문의</strong>
                  <span>평일: 09:00~18:00</span>
                </div>
              </div>
            </div>
            <div class="infoTleft">
              <div class="group1">
                <strong>상담번호 안내</strong>
                <span>1번 예약번호 및 조회</span>
                <span>2번 마일리지,제휴카드,상품권 및 기타문의</span>
              </div>
              <div class="group1">
                <p>외국인한국여행 전용상담 02-398-6600</p>
                <p>법인고객 전용상담 1566-0072</p>
                <p>안심카드결제 ARS 1577-0015</p>
                <span class="popup">카드/제휴혜택</span>
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
                footerList: [
                    {
                        id:1,
                        src:'./images/ic_group.png',
                        alt: '하나트레비즈',
                        href: 'https://www.hanatour.com/',
                        title: '하나트레비즈',
                    },
                    {
                        id:2,
                        src:'./images/ic_custom.png',
                        alt: '맞춤여행',
                        href: 'https://www.hanatour.com/',
                        title: '맞춤여행',
                    },
                    {
                        id:3,
                        src:'./images/ic_hanalive.png',
                        alt: '하나Live',
                        href: 'https://www.hanatour.com/',
                        title: '하나Live',
                    },
                    {
                        id:4,
                        src:'./images/ic_hanatourgift.png',
                        alt: '하나투어상품권',
                        href: 'https://www.hanatour.com/',
                        title: '하나투어상품권',
                    },
                    {
                        id:5,
                        src:'./images/ic_itc.png',
                        alt: '외국인여행',
                        href: 'https://www.hanatour.com/',
                        title: '외국인여행',
                    },
                    {
                        id:6,
                        src:'./images/ic_mileage.png',
                        alt: '마일리지클럽',
                        href: 'https://www.hanatour.com/',
                        title: '마일리지클럽',
                    },
                    {
                        id:7,
                        src:'./images/ic_safetyjoy.png',
                        alt: 'SAFETY&JOY',
                        href: 'https://www.hanatour.com/',
                        title: 'SAFETY&JOY',
                    },
                    {
                        id:8,
                        src:'./images/ic_zeus.png',
                        alt: '제우스',
                        href: 'https://www.hanatour.com/',
                        title: '제우스',
                    },
                ]
            }
        },
        
    }
</script>

<style>
.group1 .comm-item + .comm-item{
  margin-top: 30px;
}
  .infoTleft{
    padding: 30px 0;
    width: 282px;
  }
  .infoWrap {
    max-width: 1200px;
    margin: 0 auto;
    margin-top: 40px;
  }
  .infoWrap .inner{
    width: 100%;
    display: flex;
    align-items: flex-start;
    justify-content: space-between;
    background-color: #fff;
  }
  .infoWrap .infoTleft p{
    display: block;
    margin-top: 18px;
    font-size: 15px;
    color: #111;
    line-height: 1;
    margin-bottom: 3px;
    font-weight: 600;
  }

  .infoWrap  .infoTleft .popup{
    position: relative;
    margin-top: 7px;
    display: inline-block;
    height: 24px;
    line-height: 22px;
    font-size: 12px;
    padding: 0 12px;
    border: 1px solid #111;
    color: #666;
    background-color:  #fff;
    font-weight: 400;
    letter-spacing: -0.48px;
    text-align: center;
    border-radius: 4px;
    border: 1px solid #c2c2c2;
  }
  .infoTCenter{
    max-width: 636px;
    display: flex;
    justify-content: space-between;
    padding: 30px 0;
    gap: 0 100px;
  }

  .infoWrap .inner strong{
    display: block;
    color:#111;
    font-size: 15px;
    line-height: 1;
    margin-bottom: 3px;
  }
  .infoWrap .inner span{
    display: block;
    margin-top:6px;
    font-size: 13px;
    color: #666;
  }
  .infoWrap .inner .infoTitle {
    padding: 40px 50px;
  }
  .infoWrap .inner .infoTitle h3{
    font-weight: 600;
    font-size: 22px;
    line-height: 27px;
    color: #111;
  }
  .infoWrap .inner .infoTitle strong{
    display: block;
    font-size: 24px;
    color: #111;
    line-height: 1;
    padding: 14px 0;
    margin-bottom: 0;
  }
  .infoWrap .inner .infoTitle .link{
    position: relative;
    margin-top: 13px;
  }
  .infoWrap .inner .infoTitle .link::after{
    content: "";
    clear: both;
    position: absolute;
    right: 0;
    top: 3px;
    background: url(../../public/images/spr_btn.png)no-repeat;
    width: 13px;
    height: 14px;
    margin: 0 0 0 5px;
    display: inline-block;
    background-position: -28px 0;
  }

  .infoWrap .inner .infoTitle .link1::after{
    right: 14px;
  }


  .infoWrap .inner .infoTitle span{
    font-size: 14px;
    color: #111;
  }
  /*  */
  .berMenu{
    background-color: #eeeeee;
    padding: 20px 0;
  }
  .berMenu ul{
    max-width: 1200px;
    width: 100%;
    margin: 0 auto;
    display: flex;
    flex-wrap: wrap;
    padding: 0;
    list-style: none;
  }
  .berMenu ul li{
    width: 12.5%;
    aspect-ratio: 1 / 0.89;
    display: flex;
    justify-content: center;
    align-items: center;
    background: #fff;
    box-sizing: border-box;
  }
  .berMenu ul li a{
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    width: 100%;
    height: 100%;
  }

  .berMenu ul li img{
    width: 100%;
    max-width: 25px;
    height: auto;
    margin: 0 auto;
  }
  .berMenu ul li + li{
      border-left: 1px solid #f7f7f7;
  }
  .berMenu ul li span{
    display: block;
    padding-top: 10px;
    text-align: center;
    font-size: 16px;
    color: #333;
  }
</style>