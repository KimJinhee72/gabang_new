<template>
    <!-- 로그인 페이지 틀 -->
    <div class="bb_login-container">
      <h2 class="bb_login-title">로그인</h2>
      <p class="bb_login-sub">여행의 시작은 가방도와 함께</p>
    
      <form class="bb_login-form">
        <input type="text" placeholder="아이디를 입력해주세요" />
        <input type="password" placeholder="비밀번호를 입력하세요" />
        <button type="submit">로그인</button>
      </form>
    
      <div class="bb_login-links">
        <a href="#">아이디 찾기</a> | 
        <a href="#">비밀번호 찾기</a> | 
        <a href="#">회원가입</a>
      </div>
    
      <div class="bb_sns-login">
        <div class="bb_grayline"></div>
        <p>간편 로그인</p>
        <div class="bb_grayline"></div>
        <div class="bb_sns-icons">
          <!-- <img src="kakao_icon.png" alt="카카오" />
          <img src="naver_icon.png" alt="네이버" />
          <img src="google_icon.png" alt="구글" /> -->
        </div>
      </div>
    </div>
    
    </template>
    
    <script setup>
    
    </script>
    
    <style lang="scss" scoped>
    @use "/src/assets/_Variables.scss" as *;
    .bb_login-container {
      width: 320px;
      margin: 100px auto;
      text-align: center;
      font-family: 'Noto Sans KR', sans-serif;
    
      .bb_login-title {
        font-size: 24px;
        font-weight: bold;
        color: #005bac; // 파란색
        padding-bottom: 20px;
      }
    
      .bb_login-sub {
        font-size: 14px;
        color: #2AAAE2;
        margin-bottom: 30px;
        font-weight: bold;
      }
    
      .bb_login-form {
        display: flex;
        flex-direction: column;
        gap: 10px;
    
        input {
          padding: 12px;
          border: 1px solid #ccc;
          border-radius: 5px;
        }
    
        button {
          background-color: #005bac;
          color: #fff;
          border: none;
          padding: 12px;
          border-radius: 5px;
          cursor: pointer;
          font-weight: bold;
        }
      }
    
      .bb_login-links {
        font-weight: bold;
        margin-top: 5%;
        font-size: 13px;
        color: #333;
    
        a {
          text-decoration: none;
          color: inherit;
    
          &:hover {
            text-decoration: underline;
          }
        }
      }
    
      .bb_sns-login {
  display: flex;
  align-items: center;
  gap: 10px; // 선과 텍스트 사이 간격
  margin: 8% 0;

  .bb_grayline {
    flex: 1;
    height: 1px;
    background-color: #ccc; // 연한 회색
  }

  p {
    white-space: nowrap; // 텍스트 줄바꿈 방지
    color: $main-color;
    font-size: 14px;
    font-weight: bold;
  }
}

    }
    
      
    </style>