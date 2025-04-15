<template>
  <div class="st_wrap">
    <p class="st_header">예약조회</p>
    <div class="st_lookup">
      <input type="text" placeholder="이름" />
      <input type="tel" placeholder="연락처" />
      <input type="number" placeholder="예약번호" />
    </div>
    <router-link to="/yeyaklookup2"><button>조회하기</button></router-link>
  </div>
</template>
<script setup></script>
<style lang="scss" scoped>
@use "@/assets/Main.scss" as *;
@use "@/assets/_Variables.scss" as *;

.st_wrap {
  width: 90%;
  max-width: 700px;
  margin-top: $margin-titletopbottom;
  margin-left: auto;
  margin-right: auto;
  margin-bottom: $margin-m;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  text-align: center;
  font-family: $font-family;
}

.st_header {
  text-align: center;
  font-size: $title-font-size-s;
  margin-bottom: $margin-m;
  padding-left: $padding-sss;
  border-left: 5px solid $main-color;
}
.st_lookup {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  text-align: center;
  width: 100%;
  max-width: 700px;
  padding: 20px;
  background-color: $background-maincolor;
  border-radius: 20px;
  box-shadow: 0 0 6px rgba(0, 0, 0, 0.1);
}

input {
  width: 90%;
  max-width: 300px;
  padding: 10px;
  margin: 8px 0;
  border: 1px solid #ccc;
  border-radius: 10px;
  display: flex;
}
button {
  padding: $padding-sss $margin-ss;
  margin: $margin-ss;
  font-size: $basic-font-size-L;
  font-family: $font-family;
  color: #fff;
  background-color: $main-color;
  border: none;
  border-radius: $border-radius-sm;
  cursor: pointer;
}
button:hover {
  background-color: $hover;
}
</style>
