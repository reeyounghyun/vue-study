<template>
  <div class="main-layout">
    <div class="layout-wrap commLayout">
      <SectionVideo />
      <SectionAbout />
      <SectionInfo />
    </div>
  </div>
</template>

<script>
import SectionVideo from './SectionVideo.vue';
import SectionAbout from './SectionAbout.vue';
import SectionInfo from './SectionInfo.vue';

export default {
  components: {
    SectionVideo,
    SectionAbout,
    SectionInfo,
  },
};
</script>

<style scoped>
.main-layout {
  margin-top: 50px;
  background: url(https://image.hanatour.com/usr/manual/update/pc/main/info/011_bg.jpg) 50% 0px no-repeat;
  height: 749px;
  overflow: hidden;
  display: flex;
  align-items: center;
}
.layout-wrap{
  display: flex;
  justify-content: space-between;
  gap: 20px;
}

.layout-wrap>div{
  flex: 1;
}

</style>
