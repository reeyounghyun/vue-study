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
  box-sizing: border-box;
  aspect-ratio: 1 / 0.89;
  display: flex;
  justify-content: center;
  align-items: center;
  background: #fff;
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