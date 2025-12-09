<template>
    <div class="asideMenu">
        <div class="nav-wrap">
            <div class="nev-ber" v-for="(logo, index) in logos" :key="index">
                <div class="btn">
                    <span></span>
                    <span></span>
                    <span></span>
                </div>
                <img :src="logo.img" :alt="logo.alt">
            </div>
            <div class="side">
                <a href="#">홈</a>
                <a href="#">둘러보기</a>
                <a href="#">보관함</a>
            </div>
        </div>
        <div class="nav-list">
            <button><span>새 재생목록</span></button>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return{
            logos: [
                {
                index: 0,
                img: require('@/assets/image/on_platform_logo_dark.png'),
                alt: '유튜브'
                },
            ]
        }
    }
}
</script>

<style>


.nav-list{
    margin-top: 28px;
}

.nav-list button{
    max-width: 200px;
    display: block;
    width: 100%;
    text-align: center;
    overflow: hidden;
    padding: 10px 0;
    font-size: 15px;
    border-radius: 28px;
    background-color: #2f2f2f;
    color: #fff;
    border: none;
}

.nav-list button span{
    position: relative;
    width: 100%;
    display: block;
    font-size: 13px;
}

.nav-list button span::after{
    position: absolute;
    content: "";
    clear: both;
    left: 19%;
    top: 0;
    width: 20px;
    height: 20px;
    background: url(../assets/image/icon_add.svg) no-repeat center center;
    filter: invert(1);
}

.nev-ber{
    display: flex;
    align-items: center;
}
.btn {
    margin-right: 20px;
}
.btn span{
    display: block;
    width: 20px;
    height: 2px;
    border-radius: 6px;
    background-color: #a5a5a5;
}
.btn span + span{
    margin-top: 5px;
}
.asideMenu{
    min-width: 250px;
    box-sizing: border-box;
    padding: 20px 0 0 10px;
    border-right: 1px solid rgba(255, 255, 255, 0.122);
}

.side{
    position: relative;
    margin-top: 30px;
}
.side a{
    display: block;
    height: 24px;
    line-height: 24px;
    padding-left: 39px;
    font-size: 14px;
    text-decoration: none;
    color: #fff;
}
.side a + a{
    margin-top: 20px;
} 

.side a:nth-child(1)::after{
    content: "";
    clear: both;
    position: absolute;
    left: 0;
    top: 0;
    background: url(../assets/image/icon_home.svg) no-repeat center center;
    width: 24px;
    height: 24px;
    filter: invert(1);
}
.side a:nth-child(2){
    position: relative;
}
.side a:nth-child(2)::after{
    content: "";
    clear: both;
    position: absolute;
    left: 0;
    top: 0;
    background: url(../assets/image/icon_autorenew.svg) no-repeat center center;
    width: 24px;
    height: 24px;
    filter: invert(1);
}

.side a:nth-child(3){
    position: relative;
}

.side a:nth-child(3)::after{
    content: "";
    clear: both;
    position: absolute;
    left: 0;
    top: 0;
    background: url(../assets/image/icon_content.svg) no-repeat center center;
    width: 24px;
    height: 24px;
    filter: invert(1);
}
</style>