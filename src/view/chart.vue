<template>
    <div class="wrap">
        <div class="Search">
            <input type="text" placeholder="노래,앨범,아티스트,핏캐스트 검색" class="search-bar" />
            <button type="button" class="eventBtn">
                <span class="btnIcon"></span>
            </button>
        </div>
        <div class="tabHashtag">
            <div class="tabNav">
                <button 
                    type="button" 
                    v-for="(tab, index) in tabs" 
                    :key="index" 
                    :class="['tab-button', {active: activeTab === index}]"
                    @click="activeTab = index"
                    >
                    {{ tab.title }} 
                </button>
            </div>
            <div class="tabContents">
                <div v-for="(tab, index) in tabs" :key="index" v-show="activeTab === index" class="tab-panel">
                    <!-- 단순 텍스트 표시 -->
                    {{ tab.content }}
                    <div v-if="index === 0" class="songs-list common-list">
                        <div class="tag">
                            <span>재생목록</span>
                            <span>노래</span>
                            <span>앨범</span>
                            <span>아티스트</span>
                            <span>팟캐스트</span>
                        </div>
                        <!-- 인기곡 관련 HTML 컨텐츠 -->
                        <ul>
                            <li>
                                <span class="imgItem">
                                    <div class="itembg">
                                        <div class="textTop">
                                            <strong>Top <span>100</span></strong>
                                            <strong>SONGS</strong>
                                        </div>
                                        <span class="ko">SOUTH KOREA</span>
                                    </div>
                                </span>
                                <strong class="title ti">Ruby</strong>
                                <div class="titlechild">
                                    <p class="titlechild type">앨범</p>
                                    <p class="titlechild icon">•</p>
                                    <p class="titlechild singer">제니(JENNIE)</p>
                                </div>
                            </li>
                            <li>
                                <span class="imgItem">
                                    <div class="itembg">
                                        <div class="textTop">
                                            <strong>Top <span>100</span></strong>
                                            <strong>MUSIC VIDEOS</strong>
                                        </div>
                                        <span class="ko">SOUTH KOREA</span>
                                    </div>
                                </span>
                                <strong class="title ti">Alter Ego</strong>
                                <div class="titlechild">
                                    <p class="titlechild type">앨범</p>
                                    <p class="titlechild icon">•</p>
                                    <p class="titlechild singer">LISA</p>
                                </div>
                            </li>
                            <li>
                                <span class="imgItem">
                                    <div class="itembg">
                                        <div class="textTop">
                                            <strong>TERNDING</strong>
                                            <span>20</span>
                                        </div>
                                        <span class="ko">SOUTH KOREA</span>
                                    </div>
                                </span>
                                <strong class="title">Almond Chocolate<br/>(Korean Ver.)</strong>
                                <div class="titlechild">
                                    <p class="titlechild type">싱글</p>
                                    <p class="titlechild icon">•</p>
                                    <p class="titlechild singer">ILLIT</p>
                                </div>
                            </li>
                            <li>
                                <span class="imgItem">
                                    <div class="itembg">
                                        <img src="../assets/image/singer-img-1.png" alt="이미지">
                                    </div>
                                </span>
                                <strong class="title ti">Come Together</strong>
                                <div class="titlechild">
                                    <p class="titlechild type">앨범</p>
                                    <p class="titlechild icon">•</p>
                                    <p class="titlechild singer">비틀즈</p>
                                </div>
                            </li>
                            <li>
                                <span class="imgItem">
                                    <div class="itembg">
                                        <img src="../assets/image/singer-img-2.png" alt="이미지">
                                    </div>
                                </span>
                                <strong class="title ti">wait for the elash</strong>
                                <div class="titlechild">
                                    <p class="titlechild type">앨범</p>
                                    <p class="titlechild icon">•</p>
                                    <p class="titlechild singer">기리보이</p>
                                </div>
                            </li>
                            <li>
                                <span class="imgItem">
                                    <div class="itembg">
                                        <img src="../assets/image/singer-img-3.png" alt="이미지">
                                    </div>
                                </span>
                                <strong class="title">신호등</strong>
                                <div class="titlechild">
                                    <p class="titlechild type">싱글</p>
                                    <p class="titlechild icon">•</p>
                                    <p class="titlechild singer">이무진</p>
                                </div>
                            </li>
                            <li>
                                <span class="imgItem">
                                    <div class="itembg">
                                        <img src="../assets/image/singer-img-4.png" alt="이미지">
                                    </div>
                                </span>
                                <strong class="title">Tomboy</strong>
                                <div class="titlechild">
                                    <p class="titlechild type">싱글</p>
                                    <p class="titlechild icon">•</p>
                                    <p class="titlechild singer">(여자)아이들</p>
                                </div>
                            </li>
                            <li>
                                <span class="imgItem">
                                    <div class="itembg">
                                        <img src="../assets/image/singer-img-5.png" alt="이미지">
                                    </div>
                                </span>
                                <strong class="title">INVU </strong>
                                <div class="titlechild">
                                    <p class="titlechild type">싱글</p>
                                    <p class="titlechild icon">•</p>
                                    <p class="titlechild singer">태연</p>
                                </div>
                            </li>
                            <li>
                                <span class="imgItem">
                                    <div class="itembg">
                                        <img src="../assets/image/singer-img-6.png" alt="이미지">
                                    </div>
                                </span>
                                <strong class="title">우효</strong>
                                <div class="titlechild">
                                    <p class="titlechild type">싱글</p>
                                    <p class="titlechild icon">•</p>
                                    <p class="titlechild singer">민들레</p>
                                </div>
                            </li>
                            <li>
                                <span class="imgItem">
                                    <div class="itembg">
                                        <img src="../assets/image/singer-img-7.png" alt="이미지">
                                    </div>
                                </span>
                                <strong class="title">Spicy</strong>
                                <div class="titlechild">
                                    <p class="titlechild type">싱글</p>
                                    <p class="titlechild icon">•</p>
                                    <p class="titlechild singer">에스파</p>
                                </div>
                            </li>
                            <li>
                                <span class="imgItem">
                                    <div class="itembg">
                                        <div class="textTop">
                                            <strong>Top <span>100</span></strong>
                                            <strong>SONGS</strong>
                                        </div>
                                        <span class="ko">SOUTH KOREA</span>
                                    </div>
                                </span>
                                <strong class="title ti">Ruby</strong>
                                <div class="titlechild">
                                    <p class="titlechild type">앨범</p>
                                    <p class="titlechild icon">•</p>
                                    <p class="titlechild singer">제니(JENNIE)</p>
                                </div>
                            </li>
                            <li>
                                <span class="imgItem">
                                    <div class="itembg">
                                        <div class="textTop">
                                            <strong>Top <span>100</span></strong>
                                            <strong>MUSIC VIDEOS</strong>
                                        </div>
                                        <span class="ko">SOUTH KOREA</span>
                                    </div>
                                </span>
                                <strong class="title ti">Alter Ego</strong>
                                <div class="titlechild">
                                    <p class="titlechild type">앨범</p>
                                    <p class="titlechild icon">•</p>
                                    <p class="titlechild singer">LISA</p>
                                </div>
                            </li>
                            <li>
                                <span class="imgItem">
                                    <div class="itembg">
                                        <div class="textTop">
                                            <strong>TERNDING</strong>
                                            <span>20</span>
                                        </div>
                                        <span class="ko">SOUTH KOREA</span>
                                    </div>
                                </span>
                                <strong class="title">Almond Chocolate<br/>(Korean Ver.)</strong>
                                <div class="titlechild">
                                    <p class="titlechild type">싱글</p>
                                    <p class="titlechild icon">•</p>
                                    <p class="titlechild singer">ILLIT</p>
                                </div>
                            </li>
                            <li>
                                <span class="imgItem">
                                    <div class="itembg">
                                        <img src="../assets/image/singer-img-1.png" alt="이미지">
                                    </div>
                                </span>
                                <strong class="title ti">Come Together</strong>
                                <div class="titlechild">
                                    <p class="titlechild type">앨범</p>
                                    <p class="titlechild icon">•</p>
                                    <p class="titlechild singer">비틀즈</p>
                                </div>
                            </li>
                            <li>
                                <span class="imgItem">
                                    <div class="itembg">
                                        <img src="../assets/image/singer-img-2.png" alt="이미지">
                                    </div>
                                </span>
                                <strong class="title ti">wait for the elash</strong>
                                <div class="titlechild">
                                    <p class="titlechild type">앨범</p>
                                    <p class="titlechild icon">•</p>
                                    <p class="titlechild singer">기리보이</p>
                                </div>
                            </li>
                            <li>
                                <span class="imgItem">
                                    <div class="itembg">
                                        <img src="../assets/image/singer-img-3.png" alt="이미지">
                                    </div>
                                </span>
                                <strong class="title">신호등</strong>
                                <div class="titlechild">
                                    <p class="titlechild type">싱글</p>
                                    <p class="titlechild icon">•</p>
                                    <p class="titlechild singer">이무진</p>
                                </div>
                            </li>
                            <li>
                                <span class="imgItem">
                                    <div class="itembg">
                                        <img src="../assets/image/singer-img-4.png" alt="이미지">
                                    </div>
                                </span>
                                <strong class="title">Tomboy</strong>
                                <div class="titlechild">
                                    <p class="titlechild type">싱글</p>
                                    <p class="titlechild icon">•</p>
                                    <p class="titlechild singer">(여자)아이들</p>
                                </div>
                            </li>
                            <li>
                                <span class="imgItem">
                                    <div class="itembg">
                                        <img src="../assets/image/singer-img-5.png" alt="이미지">
                                    </div>
                                </span>
                                <strong class="title">INVU </strong>
                                <div class="titlechild">
                                    <p class="titlechild type">싱글</p>
                                    <p class="titlechild icon">•</p>
                                    <p class="titlechild singer">태연</p>
                                </div>
                            </li>
                            <li>
                                <span class="imgItem">
                                    <div class="itembg">
                                        <img src="../assets/image/singer-img-6.png" alt="이미지">
                                    </div>
                                </span>
                                <strong class="title">우효</strong>
                                <div class="titlechild">
                                    <p class="titlechild type">싱글</p>
                                    <p class="titlechild icon">•</p>
                                    <p class="titlechild singer">민들레</p>
                                </div>
                            </li>
                            <li>
                                <span class="imgItem">
                                    <div class="itembg">
                                        <img src="../assets/image/singer-img-7.png" alt="이미지">
                                    </div>
                                </span>
                                <strong class="title">Spicy</strong>
                                <div class="titlechild">
                                    <p class="titlechild type">싱글</p>
                                    <p class="titlechild icon">•</p>
                                    <p class="titlechild singer">에스파</p>
                                </div>
                            </li>
                            <li>
                                <span class="imgItem">
                                    <div class="itembg">
                                        <div class="textTop">
                                            <strong>Top <span>100</span></strong>
                                            <strong>SONGS</strong>
                                        </div>
                                        <span class="ko">SOUTH KOREA</span>
                                    </div>
                                </span>
                                <strong class="title ti">Ruby</strong>
                                <div class="titlechild">
                                    <p class="titlechild type">앨범</p>
                                    <p class="titlechild icon">•</p>
                                    <p class="titlechild singer">제니(JENNIE)</p>
                                </div>
                            </li>
                            <li>
                                <span class="imgItem">
                                    <div class="itembg">
                                        <div class="textTop">
                                            <strong>Top <span>100</span></strong>
                                            <strong>MUSIC VIDEOS</strong>
                                        </div>
                                        <span class="ko">SOUTH KOREA</span>
                                    </div>
                                </span>
                                <strong class="title ti">Alter Ego</strong>
                                <div class="titlechild">
                                    <p class="titlechild type">앨범</p>
                                    <p class="titlechild icon">•</p>
                                    <p class="titlechild singer">LISA</p>
                                </div>
                            </li>
                            <li>
                                <span class="imgItem">
                                    <div class="itembg">
                                        <div class="textTop">
                                            <strong>TERNDING</strong>
                                            <span>20</span>
                                        </div>
                                        <span class="ko">SOUTH KOREA</span>
                                    </div>
                                </span>
                                <strong class="title">Almond Chocolate<br/>(Korean Ver.)</strong>
                                <div class="titlechild">
                                    <p class="titlechild type">싱글</p>
                                    <p class="titlechild icon">•</p>
                                    <p class="titlechild singer">ILLIT</p>
                                </div>
                            </li>
                            <li>
                                <span class="imgItem">
                                    <div class="itembg">
                                        <img src="../assets/image/singer-img-1.png" alt="이미지">
                                    </div>
                                </span>
                                <strong class="title ti">Come Together</strong>
                                <div class="titlechild">
                                    <p class="titlechild type">앨범</p>
                                    <p class="titlechild icon">•</p>
                                    <p class="titlechild singer">비틀즈</p>
                                </div>
                            </li>
                            <li>
                                <span class="imgItem">
                                    <div class="itembg">
                                        <img src="../assets/image/singer-img-2.png" alt="이미지">
                                    </div>
                                </span>
                                <strong class="title ti">wait for the elash</strong>
                                <div class="titlechild">
                                    <p class="titlechild type">앨범</p>
                                    <p class="titlechild icon">•</p>
                                    <p class="titlechild singer">기리보이</p>
                                </div>
                            </li>
                            <li>
                                <span class="imgItem">
                                    <div class="itembg">
                                        <img src="../assets/image/singer-img-3.png" alt="이미지">
                                    </div>
                                </span>
                                <strong class="title">신호등</strong>
                                <div class="titlechild">
                                    <p class="titlechild type">싱글</p>
                                    <p class="titlechild icon">•</p>
                                    <p class="titlechild singer">이무진</p>
                                </div>
                            </li>
                            <li>
                                <span class="imgItem">
                                    <div class="itembg">
                                        <img src="../assets/image/singer-img-4.png" alt="이미지">
                                    </div>
                                </span>
                                <strong class="title">Tomboy</strong>
                                <div class="titlechild">
                                    <p class="titlechild type">싱글</p>
                                    <p class="titlechild icon">•</p>
                                    <p class="titlechild singer">(여자)아이들</p>
                                </div>
                            </li>
                            <li>
                                <span class="imgItem">
                                    <div class="itembg">
                                        <img src="../assets/image/singer-img-5.png" alt="이미지">
                                    </div>
                                </span>
                                <strong class="title">INVU </strong>
                                <div class="titlechild">
                                    <p class="titlechild type">싱글</p>
                                    <p class="titlechild icon">•</p>
                                    <p class="titlechild singer">태연</p>
                                </div>
                            </li>
                            <li>
                                <span class="imgItem">
                                    <div class="itembg">
                                        <img src="../assets/image/singer-img-6.png" alt="이미지">
                                    </div>
                                </span>
                                <strong class="title">우효</strong>
                                <div class="titlechild">
                                    <p class="titlechild type">싱글</p>
                                    <p class="titlechild icon">•</p>
                                    <p class="titlechild singer">민들레</p>
                                </div>
                            </li>
                            <li>
                                <span class="imgItem">
                                    <div class="itembg">
                                        <img src="../assets/image/singer-img-7.png" alt="이미지">
                                    </div>
                                </span>
                                <strong class="title">Spicy</strong>
                                <div class="titlechild">
                                    <p class="titlechild type">싱글</p>
                                    <p class="titlechild icon">•</p>
                                    <p class="titlechild singer">에스파</p>
                                </div>
                            </li>
                            <li>
                                <span class="imgItem">
                                    <div class="itembg">
                                        <div class="textTop">
                                            <strong>Top <span>100</span></strong>
                                            <strong>SONGS</strong>
                                        </div>
                                        <span class="ko">SOUTH KOREA</span>
                                    </div>
                                </span>
                                <strong class="title ti">Ruby</strong>
                                <div class="titlechild">
                                    <p class="titlechild type">앨범</p>
                                    <p class="titlechild icon">•</p>
                                    <p class="titlechild singer">제니(JENNIE)</p>
                                </div>
                            </li>
                            <li>
                                <span class="imgItem">
                                    <div class="itembg">
                                        <div class="textTop">
                                            <strong>Top <span>100</span></strong>
                                            <strong>MUSIC VIDEOS</strong>
                                        </div>
                                        <span class="ko">SOUTH KOREA</span>
                                    </div>
                                </span>
                                <strong class="title ti">Alter Ego</strong>
                                <div class="titlechild">
                                    <p class="titlechild type">앨범</p>
                                    <p class="titlechild icon">•</p>
                                    <p class="titlechild singer">LISA</p>
                                </div>
                            </li>
                            <li>
                                <span class="imgItem">
                                    <div class="itembg">
                                        <div class="textTop">
                                            <strong>TERNDING</strong>
                                            <span>20</span>
                                        </div>
                                        <span class="ko">SOUTH KOREA</span>
                                    </div>
                                </span>
                                <strong class="title">Almond Chocolate<br/>(Korean Ver.)</strong>
                                <div class="titlechild">
                                    <p class="titlechild type">싱글</p>
                                    <p class="titlechild icon">•</p>
                                    <p class="titlechild singer">ILLIT</p>
                                </div>
                            </li>
                            <li>
                                <span class="imgItem">
                                    <div class="itembg">
                                        <img src="../assets/image/singer-img-1.png" alt="이미지">
                                    </div>
                                </span>
                                <strong class="title ti">Come Together</strong>
                                <div class="titlechild">
                                    <p class="titlechild type">앨범</p>
                                    <p class="titlechild icon">•</p>
                                    <p class="titlechild singer">비틀즈</p>
                                </div>
                            </li>
                            <li>
                                <span class="imgItem">
                                    <div class="itembg">
                                        <img src="../assets/image/singer-img-2.png" alt="이미지">
                                    </div>
                                </span>
                                <strong class="title ti">wait for the elash</strong>
                                <div class="titlechild">
                                    <p class="titlechild type">앨범</p>
                                    <p class="titlechild icon">•</p>
                                    <p class="titlechild singer">기리보이</p>
                                </div>
                            </li>
                            <li>
                                <span class="imgItem">
                                    <div class="itembg">
                                        <img src="../assets/image/singer-img-3.png" alt="이미지">
                                    </div>
                                </span>
                                <strong class="title">신호등</strong>
                                <div class="titlechild">
                                    <p class="titlechild type">싱글</p>
                                    <p class="titlechild icon">•</p>
                                    <p class="titlechild singer">이무진</p>
                                </div>
                            </li>
                            <li>
                                <span class="imgItem">
                                    <div class="itembg">
                                        <img src="../assets/image/singer-img-4.png" alt="이미지">
                                    </div>
                                </span>
                                <strong class="title">Tomboy</strong>
                                <div class="titlechild">
                                    <p class="titlechild type">싱글</p>
                                    <p class="titlechild icon">•</p>
                                    <p class="titlechild singer">(여자)아이들</p>
                                </div>
                            </li>
                            <li>
                                <span class="imgItem">
                                    <div class="itembg">
                                        <img src="../assets/image/singer-img-5.png" alt="이미지">
                                    </div>
                                </span>
                                <strong class="title">INVU </strong>
                                <div class="titlechild">
                                    <p class="titlechild type">싱글</p>
                                    <p class="titlechild icon">•</p>
                                    <p class="titlechild singer">태연</p>
                                </div>
                            </li>
                            <li>
                                <span class="imgItem">
                                    <div class="itembg">
                                        <img src="../assets/image/singer-img-6.png" alt="이미지">
                                    </div>
                                </span>
                                <strong class="title">우효</strong>
                                <div class="titlechild">
                                    <p class="titlechild type">싱글</p>
                                    <p class="titlechild icon">•</p>
                                    <p class="titlechild singer">민들레</p>
                                </div>
                            </li>
                            <li>
                                <span class="imgItem">
                                    <div class="itembg">
                                        <img src="../assets/image/singer-img-7.png" alt="이미지">
                                    </div>
                                </span>
                                <strong class="title">Spicy</strong>
                                <div class="titlechild">
                                    <p class="titlechild type">싱글</p>
                                    <p class="titlechild icon">•</p>
                                    <p class="titlechild singer">에스파</p>
                                </div>
                            </li>
                            <li>
                                <span class="imgItem">
                                    <div class="itembg">
                                        <div class="textTop">
                                            <strong>Top <span>100</span></strong>
                                            <strong>SONGS</strong>
                                        </div>
                                        <span class="ko">SOUTH KOREA</span>
                                    </div>
                                </span>
                                <strong class="title ti">Ruby</strong>
                                <div class="titlechild">
                                    <p class="titlechild type">앨범</p>
                                    <p class="titlechild icon">•</p>
                                    <p class="titlechild singer">제니(JENNIE)</p>
                                </div>
                            </li>
                            <li>
                                <span class="imgItem">
                                    <div class="itembg">
                                        <div class="textTop">
                                            <strong>Top <span>100</span></strong>
                                            <strong>MUSIC VIDEOS</strong>
                                        </div>
                                        <span class="ko">SOUTH KOREA</span>
                                    </div>
                                </span>
                                <strong class="title ti">Alter Ego</strong>
                                <div class="titlechild">
                                    <p class="titlechild type">앨범</p>
                                    <p class="titlechild icon">•</p>
                                    <p class="titlechild singer">LISA</p>
                                </div>
                            </li>
                            <li>
                                <span class="imgItem">
                                    <div class="itembg">
                                        <div class="textTop">
                                            <strong>TERNDING</strong>
                                            <span>20</span>
                                        </div>
                                        <span class="ko">SOUTH KOREA</span>
                                    </div>
                                </span>
                                <strong class="title">Almond Chocolate<br/>(Korean Ver.)</strong>
                                <div class="titlechild">
                                    <p class="titlechild type">싱글</p>
                                    <p class="titlechild icon">•</p>
                                    <p class="titlechild singer">ILLIT</p>
                                </div>
                            </li>
                            <li>
                                <span class="imgItem">
                                    <div class="itembg">
                                        <img src="../assets/image/singer-img-1.png" alt="이미지">
                                    </div>
                                </span>
                                <strong class="title ti">Come Together</strong>
                                <div class="titlechild">
                                    <p class="titlechild type">앨범</p>
                                    <p class="titlechild icon">•</p>
                                    <p class="titlechild singer">비틀즈</p>
                                </div>
                            </li>
                            <li>
                                <span class="imgItem">
                                    <div class="itembg">
                                        <img src="../assets/image/singer-img-2.png" alt="이미지">
                                    </div>
                                </span>
                                <strong class="title ti">wait for the elash</strong>
                                <div class="titlechild">
                                    <p class="titlechild type">앨범</p>
                                    <p class="titlechild icon">•</p>
                                    <p class="titlechild singer">기리보이</p>
                                </div>
                            </li>
                            <li>
                                <span class="imgItem">
                                    <div class="itembg">
                                        <img src="../assets/image/singer-img-3.png" alt="이미지">
                                    </div>
                                </span>
                                <strong class="title">신호등</strong>
                                <div class="titlechild">
                                    <p class="titlechild type">싱글</p>
                                    <p class="titlechild icon">•</p>
                                    <p class="titlechild singer">이무진</p>
                                </div>
                            </li>
                            <li>
                                <span class="imgItem">
                                    <div class="itembg">
                                        <img src="../assets/image/singer-img-4.png" alt="이미지">
                                    </div>
                                </span>
                                <strong class="title">Tomboy</strong>
                                <div class="titlechild">
                                    <p class="titlechild type">싱글</p>
                                    <p class="titlechild icon">•</p>
                                    <p class="titlechild singer">(여자)아이들</p>
                                </div>
                            </li>
                            <li>
                                <span class="imgItem">
                                    <div class="itembg">
                                        <img src="../assets/image/singer-img-5.png" alt="이미지">
                                    </div>
                                </span>
                                <strong class="title">INVU </strong>
                                <div class="titlechild">
                                    <p class="titlechild type">싱글</p>
                                    <p class="titlechild icon">•</p>
                                    <p class="titlechild singer">태연</p>
                                </div>
                            </li>
                            <li>
                                <span class="imgItem">
                                    <div class="itembg">
                                        <img src="../assets/image/singer-img-6.png" alt="이미지">
                                    </div>
                                </span>
                                <strong class="title">우효</strong>
                                <div class="titlechild">
                                    <p class="titlechild type">싱글</p>
                                    <p class="titlechild icon">•</p>
                                    <p class="titlechild singer">민들레</p>
                                </div>
                            </li>
                            <li>
                                <span class="imgItem">
                                    <div class="itembg">
                                        <img src="../assets/image/singer-img-7.png" alt="이미지">
                                    </div>
                                </span>
                                <strong class="title">Spicy</strong>
                                <div class="titlechild">
                                    <p class="titlechild type">싱글</p>
                                    <p class="titlechild icon">•</p>
                                    <p class="titlechild singer">에스파</p>
                                </div>
                            </li>
                        </ul>
                    </div>
                    <div v-else-if="index === 1" class="listened-list common-list">
                        <div class="tag">
                            <span>재생목록</span>
                            <span>팟캐스트</span>
                            <span>노래</span>
                            <span>앨범</span>
                        </div>
                        <!-- 다시 듣기 관련 HTML 컨텐츠 -->
                        <div class="not-contant">
                            <img src="../assets/image/img_top_v1_240710.png" alt='아이콘'/>
                            <p>오프라인 저장한 음악과 팟캐스가 여기에 표시됩니다.</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>

    export default {
        data(){
            return{
                activeTab: 0,
                tabs:[
                    {title: '보관함', content: ''},
                    {title: '오프라인 저장', content: ''},
                ]
            }
        }
    }
</script>

<style>

.wrap{
    width: 100%;
    padding: 20px 0 0 80px;
}
.wrap .Search{
    overflow: hidden;
    position: relative;
}
.wrap .Search .search-bar{
    position: relative;
    border: 0.5px solid #3c3c3c;
    box-sizing: border-box;
    background-color: rgb(35 34 34);
    color: #ffffff;
    font-size: 14px;
    padding: 10px 20px;
    display: block;
    padding: 0 20px;
    height: 40.4px;
    line-height: 40.4px;
    border-radius: 5px;
    width: 500px;
}
.Search .search-bar::placeholder{
    color: rgba(255, 255, 255, 0.671);
    padding-left: 30px;
    padding-top: 10px;
    transform: translateY(2px);
    letter-spacing: 1px;

}
.wrap .Search input{
    overflow: hidden!important;;
}
/* 검색창 input */

.wrap .Search .eventBtn{
    position: absolute;
    top: 10px;
    left: 16px;
    width: 15px;
    border: 1.2px solid #888888;
    border-radius: 15px;
    aspect-ratio: 1 / 1;
    background-color: rgb(35 34 34);
}
.wrap .Search .btnIcon{
    position: absolute;
    left: 15px;
    top: 11px;
    width: 1.75px;
    height: 10px;
    border-radius: 3px 3px 5px 5px;
    transform: rotate(309deg);
    background-color: rgba(255, 255, 255, 0.4);
}

.tabHashtag .tabNav{
    display: flex;
    justify-content: flex-start;
    align-items: center;
    gap: 10px;
    margin-top: 30px;
}
.tabHashtag .tabNav button{
    display: inline-block;
    padding: 5px;
    background-color: transparent;
    border:none;
    text-align: center;
    font-size: 13px;
    color: #fff;
}

.tabHashtag .tabNav .tab-button.active{
    position: relative;
}

.tabHashtag .tabNav .tab-button.active::after{
    content: "";
    clear: both;
    position: absolute;
    bottom: -5px;
    left: 0;
    width: 100%;
    height: 2px;
    background-color: #fff;
}
.tabContents{
    margin: 30px 0;
}

.tab-panel{
    width: 100%;
}

.tag{
    display: flex;
    justify-content: flex-start;
    align-items: center;
    gap: 10px;
    margin-top: 30px;
}
.tag span{
    display: inline-block;
    padding: 5px;
    background-color: rgba(128, 128, 128, 0.388);
    border: 1px solid #000;
    text-align: center;
    border-radius: 5px;
    font-size: 13px;
    color: #fff;
}

.common-list ul{
    display: flex;
    align-items: flex-start;
    flex-wrap: wrap;
    gap: 20px;
    margin-top: 37px;
}

.common-list ul li .imgItem{
    overflow: hidden;
    position: relative;
    display: block;
    width: 150px;
    height: 150px;
    background-color: #525151;
    border-radius: 2px;
    /* 추가: 전환 효과를 위한 기본 상태 설정 */
    transition: all 0.3s ease;
    cursor: pointer;
}
.common-list ul li .imgItem::after{
    content: '';
    position: absolute;
    top:50%;
    left: 50%;
    font-size: 46px;
    font-weight: bold;
    transform: translate(-50%, -50%);
}
.common-list ul li .imgItem:hover::after{
    display: block;
    content: '';
    position: absolute;
    width: 152px;
    height: 36%;
    background: linear-gradient(to bottom, rgb(44 44 44 / 37%), rgba(0, 0, 0, 0));
    top: 27px;
    right: 0;
    z-index: 10;
    border-radius: 0 0 20px 20px;
    z-index: 10;

    /* 추가: hover 효과에 대한 transition */
    transition: opacity 0.5s, transform 0.3s;
    /* 추가: hover 시 시작할 때 약간 투명하게 */
    opacity: 0;
}

/* 추가: hover 시 after 요소가 완전히 표시되도록 */
.common-list ul li .imgItem:hover::after {
    opacity: 1;
}

.common-list ul li .imgItem .itembg{
    background: #fff;
    height: 100%;
    position: absolute;
    width: 100%;
    padding: 15px 10px;
    box-sizing: border-box;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
}

.common-list ul li .imgItem .itembg .textTop{
    line-height: 1.2;
}

.common-list ul li .imgItem strong{
    display: flex;
    font-size: 17px;
    color: #000;
    font-weight: 600;
}
.common-list ul li .imgItem span{
    display: block;
    font-size: 19px;
    color: #000;
    font-weight: 400;
}
.common-list ul li .imgItem span.ko{
    font-size: 10px;
    color: #333;
    font-weight: 400;
}

.common-list ul li .title{
    display: block;
    margin-bottom: 10px;
    margin-top: 18px;
    font-size: 14px;
    font-weight: 500;
    line-height: 1.25;
}
.common-list ul li .title:hover{
    text-decoration: underline;
}

.common-list ul li .singer:hover{
    text-decoration: underline;
}

.common-listt ul li .title.ti{
    margin-bottom: 28px;
}

.common-list ul li .titlechild{
    display: flex;
    align-items: center;
    gap: 5px;
    font-size: 14px;
    cursor: pointer;
}

/* 인기음악 */
.listened-list ul li .imgItem{
    overflow: hidden;
    position: relative;
    display: block;
    width: 150px;
    height: 150px;
    background-color: #525151;
    border-radius: 2px;
    /* 추가: 전환 효과를 위한 기본 상태 설정 */
    
    transition: all 0.3s ease;
}

.listened-list  ul li .imgItem::after{
    content: '';
    position: absolute;
    top:50%;
    left: 50%;
    font-size: 46px;
    font-weight: bold;
    transform: translate(-50%, -50%);
}

.listened-list ul li .imgItem .itembg{
    position: absolute;
    display: flex;
    justify-content: center;
    align-items: stretch;
    flex-direction: row;
    height: 100%;
    width: 100%;
    padding: 0;
}

.listened-list ul li .imgItem:hover::after{
    display: block;
    content: '';
    position: absolute;
    width: 152px;
    height: 36%;
    background: linear-gradient(to bottom, rgb(44 44 44 / 37%), rgba(0, 0, 0, 0));
    top: 27px;
    right: 0;
    z-index: 10;
    border-radius: 0 0 20px 20px;
    z-index: 10;

    /* 추가: hover 효과에 대한 transition */
    transition: opacity 0.5s, transform 0.3s;
    /* 추가: hover 시 시작할 때 약간 투명하게 */
    opacity: 0;
}

.listened-list {
    width: 100%;
}
.listened-list ul li .imgItem:hover::after {
    opacity: 1;
}
.not-contant{
    width: 100%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    padding: 22% 0;
}
.not-contant img{
    width: 30px;
    height: auto;
    margin-bottom: 12px;
    filter: brightness(0.5);
}
.not-contantt p{
    display: block;
    font-size: 12px;
    color: #fff;
}
</style>