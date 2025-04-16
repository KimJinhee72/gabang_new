<template>
  <div class="ft_footer">
    <div class="inner">
      <!-- 풋터 상단 -->
      <div class="ft_footerTop">
        <!-- 풋터 상단 왼쪽 -->
        <div class="ft_topLeft">
          <div class="ft_serviceInfo">
            <a href="#">개인정보취급방침</a>|
            <a href="#">이용약관</a>
          </div>
          <div class="ft_corpInfo">
            <p>
              대표자 : 도용달 | 사업자등록번호 053-123-4567 <br />
              주&nbsp;&nbsp;&nbsp;소 : 대구광역시 신천구 신천동로 888
              (대구광역시 신천구 신천동33-3)
              <br />
              이메일 : yongdaldo@email.com | 팩스번호 : 053-123-5678
            </p>
          </div>
          <div class="ft_accountAddress">
            <p>
              결&nbsp;제&nbsp;계&nbsp;좌 : 대구은행 123-456-78910
              <strong>가방도 도용달 </strong><br />
              택&nbsp;배&nbsp;주&nbsp;소 : 대구광역시 신천구 신천동로 888
              (우:45023)
            </p>
          </div>
        </div>
        <!-- 풋터 상단 오른쪽 -->
        <div class="ft_contactUs">
          <h1>고객센터</h1>
          <h2>123-456-7891</h2>
          <p>평&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;일 : 09:00 - 18:00</p>
          <p>토&nbsp;요&nbsp;일 : 09:00 - 13:00</p>
          <p>
            일&nbsp;요&nbsp;일 , 공&nbsp;휴&nbsp;일 : 휴 무(&nbsp; 예약일정에
            따라 변동&nbsp; )
          </p>
        </div>
      </div>
    </div>
  </div>
  <!-- 고정 버튼들 -->
  <div class="fixed-buttons">
    <button class="inquiry-btn goTopbtn" @click="scrollToTop">
      <i class="fas fa-arrow-up"></i>
      <span>위로가기</span>
    </button>
    <button class="inquiry-btn" @click="openInquiry">
      <i class="fas fa-comment"></i>
      <span>간편문의하기</span>
    </button>
    <button class="inquiry-btn" @click="openReservation">
      <i class="fas fa-calendar-check"></i>
      <span>예약하기</span>
    </button>
  </div>
</template>

<script setup>
const scrollToTop = () => {
  window.scrollTo({
    top: 0,
    behavior: "smooth",
  });
};

const openInquiry = () => {
  // 간편문의하기 기능 구현
  console.log("간편문의하기 클릭");
};

const openReservation = () => {
  // 예약하기 기능 구현
  console.log("예약하기 클릭");
};
</script>

<style lang="scss" scoped>
.ft_footer {
  width: 100%;
  background-color: #f5f5f5;
  padding: 30px 0;
  position: relative;
}

.inner {
  width: 100%;
  max-width: 1300px;
  margin: 0 auto;
  padding: 0 20px;
}

.ft_footerTop {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  gap: 40px;
}

.ft_topLeft {
  flex: 1;
}

.ft_contactUs {
  flex: 1;
  padding-left: 40px;
  border-left: 1px solid #ddd;
  min-width: 0;

  h1 {
    font-size: 18px;
    color: #333;
    margin-bottom: 8px;
    font-weight: 600;
  }

  h2 {
    font-size: 24px;
    color: #0066b3;
    margin-bottom: 12px;
    font-weight: 700;
  }

  p {
    color: #666;
    line-height: 1.6;
    font-size: 14px;
    margin-bottom: 8px;
  }
}

.ft_serviceInfo {
  margin-bottom: 15px;

  a {
    color: #333;
    text-decoration: none;
    // margin: 0 10px;

    &:hover {
      color: #0066b3;
    }
  }
}

.ft_corpInfo,
.ft_accountAddress {
  margin-bottom: 10px;

  p {
    color: #666;
    line-height: 1.5;
    font-size: 13px;
  }
}
// 고정버튼들
.fixed-buttons {
  position: fixed;
  right: 50%;
  bottom: 20px;
  transform: translateX(40%);
  width: 100%;
  max-width: 1550px;
  right: 20px;
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 8px;
  z-index: 1000;
}
.contactUs {
  display: flex;
  flex-direction: column;
}
.inquiry-btn {
  background-color: #0066b3;
  color: white;
  border: none;
  border-radius: 50px;
  padding: 10px 20px;
  font-size: 13px;
  cursor: pointer;
  box-shadow: 0 2px 10px rgba(0, 0, 0, 0.2);
  transition: all 0.3s ease;

  i {
    font-size: 14px;
  }

  &:hover {
    transform: translateY(-2px);
  }

  &:nth-child(1) {
    background-color: #666;
    &:hover {
      background-color: #444;
    }
  }

  &:nth-child(2) {
    background-color: #0066b3;
    &:hover {
      background-color: #162b50;
    }
  }

  &:nth-child(3) {
    background-color: #ff6b6b;
    &:hover {
      background-color: #ff5252;
    }
  }
}
.goTop {
}
@media screen and (max-width: 1024px) {
  .ft_footerTop {
    flex-direction: column;
    gap: 30px;
  }

  .ft_contactUs {
    flex: none;
    width: 100%;
    padding-left: 0;
    border-left: none;
    border-top: 1px solid #ddd;
    padding-top: 30px;
  }
}

@media screen and (max-width: 768px) {
  .ft_footer {
    padding: 20px 0;
  }

  .inner {
    padding: 0 15px;
  }

  .fixed-buttons {
    right: 15px;
    bottom: 15px;
  }

  .inquiry-btn {
    padding: 8px 15px;
    font-size: 12px;

    i {
      font-size: 12px;
    }
  }

  .ft_contactUs {
    h1 {
      font-size: 16px;
    }

    h2 {
      font-size: 20px;
    }

    p {
      font-size: 13px;
    }
  }
}

@media screen and (max-width: 480px) {
  .ft_footer {
    padding: 15px 0;
  }

  .inner {
    padding: 0 10px;
  }

  .ft_footerTop {
    gap: 15px;
  }

  .ft_contactUs {
    padding-top: 15px;
  }

  .fixed-buttons {
    right: 10px;
    bottom: 10px;
  }

  .inquiry-btn {
    padding: 6px 12px;
    font-size: 11px;

    i {
      font-size: 11px;
    }
  }

  .ft_contactUs {
    h1 {
      font-size: 15px;
    }

    h2 {
      font-size: 18px;
    }

    p {
      font-size: 12px;
    }
  }
}
</style>
