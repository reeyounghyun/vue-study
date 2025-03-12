<template>
    <div class="asideMenu">
        <div class="nev-ber" v-for="(logo, index) in logos" :key="index">
            <div class="btn">
                <span></span>
                <span></span>
                <span></span>
            </div>
            <img :src="logo.img" :alt="logo.alt">
            
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

<style scoped>
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
}
</style>