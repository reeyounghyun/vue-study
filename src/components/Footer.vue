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
</style>