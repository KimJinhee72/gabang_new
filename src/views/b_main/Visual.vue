<template>
  <div class="ma_visual-wrap">
    <div class="inner">
      <!-- 왼쪽 -->
      <div class="mavistxt">
        <h4>가방도는 당신의 짐을 대신 들어드립니다</h4>
        <div class="ma_vis_h1">
        <h1 class="">짐은 원하는 곳에 맡기고 받기</h1>    </div>
        <h1 class="mablue">지금 맡기세요!</h1>
        <button>예약하기</button>
      </div>
      <!-- 오른쪽 -->
      <div class="mavisimg">
        <!-- <img src="/public/images/ma/ma_visual/mavisual.gif" alt="ma-viusal" /> -->
        <img src="/public/images/gh/ma_visual/mavisual.gif" alt="ma-viusal" />
        <!-- 오디오 음악재생 -->
        <audio autoplay controls class="mavisaudio" loop>
          <!-- <source src="/public/music.mp3" /> -->
          <source src="/public/images/gh/music.mp3" />
        </audio>
      </div>
    </div>
  </div>
</template>
<script setup></script>
<style scoped>
/* 전체영역 */
.ma_visual-wrap .inner {
  width: 100%;
  max-width: 1300px;
  margin-top: 50px;
 
  display: flex;
  justify-content: flex-end;
  margin: auto;
  /* background-color: antiquewhite; */
}
/* 왼쪽 - 텍스트박스  */
.mavistxt {
  margin: 13% 0;
  /* margin-right: 5%; */
  width: 25%;
  text-align: right;
  display: flex;
  flex-direction: column;
  align-items: flex-end;
}
.ma_vis_h1 h1:first-child{
  font-size: 20px !important;
  line-height: 30px !important;
  /* text-align: center; */
}
.mavistxt > h4 {
  width: 300px;
  font-size: 16px;
  color: #5a5a5a;
  margin-bottom: 10px;

}
.mavistxt > h1 , .ma_vis_h1 h1 {
  font-size: 40px;
  color: #5a5a5a;
  line-height: 50px;
  
}
.ma_vis_h1{
display: flex;
justify-content: right;
gap: 10px;
}
/* 맡기세요! (문구- 블루) */
.mablue {
  width: 230px;
  color: #0066b3 !important;
  padding: 20px 0 !important;
}
.mavistxt > button {
  width: 145px;
  height: 50px;
  font-size: 19px;
  background: #0066b3;
  color: white;
  border: none;
  border-radius: 20px;
  cursor: pointer;
  transition: 0.3s;
  margin-top: 20px;
  text-align: center;
  span{
    font-size: 21px;
    margin-left: 5px;
  };
}
.mavistxt > button:hover {
  background: #162b50;
}
/* 오른쪽 - gif이미지 */
.mavisimg {
  position: relative;
  width: 70%;
  /* min-width: 390px; */
}
.mavisimg > img {
  width: 100%;
  padding: 0px 50px 50px 50px;
}
audio {
  width: 100%;
  max-width: 100px; /* 적절한 크기로 제한 */
  height: 30px;
  background-color: #fff !important; /* 배경색 변경 */
  border-radius: 10px; /* 둥근 모서리 */
  position: absolute;
  bottom: 50px;
  right: 0px;
}


</style>
