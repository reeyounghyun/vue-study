<template>
  <div class="wrap">
    <div class="Contents">
      <div class="imageBox">
        <img :src="require('@/assets/image/file.png')" alt="오늘의노래">
      </div>
      <div class="textBox">
        <h2>이달의 노래 10월 (2024)</h2>
        <span>VIBE</span>
        <div class="day">
          <span class="toDay">2024.10.07</span>
          <span class="toTime">2시간 51분</span>
          <p>2024년 10월 선정된 이달의 노래! 지난 한 달간 VIBE에서 많은 사랑을 받았던 곡들을 한번에 감상해보세요. 마음에 드는 곡은 좋아요를 눌러 보관함에 담아두세요.</p>
        </div>
        <div class="btnWrap">
          <div class="btnBox">
            <button class="palyAll" @click="playAll"><span>전체재생</span></button>
            <button class="playRandom" @click="playRandom"><span>램덤재생</span></button>
            <button class="buyMP3" @click="buyMP3"><span>MP3구매</span></button>
          </div>
          <div class="otherBut">
            <button class="likeIcon" @click="likeIcon">
              <span class="material-icons">favorite</span>
            </button>
            <button class="otherIcon" @click="otherIcon">
              <span class="material-icons">play_circle</span>
            </button>
          </div>
        </div>
      </div>
    </div>
    <div class="musicList custom-checkbox">
      <ul>
        <li v-for="(list, index) in musicListItem" :key="index">
          <input type="checkbox" :id="'checkbox-' + index" v-model="list.isChecked">
          <label :for="'checkbox-' + index"></label>
          <img :src="list.checkSrc" :alt="list.checkAlt">
          <span class="title">{{ list.title }}</span>
          <div class="titleItem">
            <span class="singer">{{ list.singer }}</span>
            <span class="group">{{ list.group }}</span>
          </div>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
const fileImage = require('@/assets/image/32076760.jpg');
const fileImage1 = require('@/assets/image/32004180.jpg');
const fileImage2 = require('@/assets/image/32056801.jpg');

export default {
  data() {
    return {
      musicListItem: [
        {
          checkSrc: fileImage,
          checkAlt: '녹아내려요',
          title: '녹아내려요',
          singer: 'DAY6(데이식스)',
          group: 'Band Aid',
          isChecked: false
        },
        {
          checkSrc: fileImage1,
          checkAlt: '별별별(See that?)',
          title: '별별별(See that?)',
          singer: 'NMIXX',
          group: 'Fe3O4: STICK OUT',
          isChecked: false
        },
        {
          checkSrc: fileImage2,
          checkAlt: 'CRAZY',
          title: 'CRAZY',
          singer: 'LE SSERAFIM (르세라핌)',
          group: 'CRAZY',
          isChecked: false
        },
        {
          checkSrc: fileImage,
          checkAlt: '녹아내려요',
          title: '녹아내려요',
          singer: 'DAY6(데이식스)',
          group: 'Band Aid',
          isChecked: false
        },
        {
          checkSrc: fileImage1,
          checkAlt: '별별별(See that?)',
          title: '별별별(See that?)',
          singer: 'NMIXX',
          group: 'Fe3O4: STICK OUT',
          isChecked: false
        },
        {
          checkSrc: fileImage2,
          checkAlt: 'CRAZY',
          title: 'CRAZY',
          singer: 'LE SSERAFIM (르세라핌)',
          group: 'CRAZY',
          isChecked: false
        },
      ]
    };
  },
  methods: {
    playAll() {
      console.log("전체 재생 클릭");
    },
    playRandom() {
      console.log("랜덤 재생 클릭");
    },
    buyMP3() {
      console.log("MP3 구매");
    }
  }
};
</script>

<style scoped>
.wrap{
  width: 100%;
}   
.custom-checkbox {
  position: relative;
}

/* 기본 체크박스 숨기기 */
.custom-checkbox input[type="checkbox"] {
  position: absolute;
  opacity: 0;
  cursor: pointer;
}

/* 커스텀 체크박스 디자인 */
.custom-checkbox label {
  position: absolute;
    top: 15px;
    left: 8px;
    width: 20px;
    height: 20px;
    border: 2px solid #ccc;
    border-radius: 3px;
    cursor: pointer;
}

/* 체크 표시 스타일 */
.custom-checkbox label:after {
  content: '';
  position: absolute;
  display: none;
  left: 6px;
  top: 2px;
  width: 5px;
  height: 10px;
  border: solid white;
  border-width: 0 2px 2px 0;
  transform: rotate(45deg);
}

/* 체크박스가 체크되었을 때의 배경색 */
.custom-checkbox input[type="checkbox"]:checked + label {
  border-color: #474747;  /* 체크됐을 때 테두리 색상 */
}

/* 체크박스가 체크되었을 때 체크 표시 보이기 */
.custom-checkbox input[type="checkbox"]:checked + label:after {
  display: block;
}

</style>
