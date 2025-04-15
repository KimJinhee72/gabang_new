<template>
  <!-- 수정 -->
  <!-- 전체 -->
  <div class="bb_wrap">
    <!-- 전체 이너 -->
    <div class="bb_inner">
      <!-- 이용절차 -->
      <div class="bb_container1">
        <!-- 타이틀 1-->
        <div class="bb_title1">
          <!-- 제목 스타일 -->
          <div class="bb_titleLine"></div>
          <!-- 제목 -->
          <div class="title_txt1">
            <h1>짐운송 이용절차</h1>
          </div>
        </div>
        <!-- 아이콘설명 -->
        <div class="bb_orderProcess">
          <!-- 아이콘1 -->
          <div class="bb_processIcon1">
            <!-- 아이콘1_이미지 -->
            <div class="bb_processIcon1_img">
              <img src="/public/images/yr/page1/1p_icon1.png" alt="icon1" />
            </div>
            <!-- 아이콘1_글 -->
            <span>예약/결제</span>
          </div>
          <!-- 화살표 -->
          <div class="arrow">
            <img src="/public/images/yr/page1/arrow.png" alt="arrow1" />
          </div>
          <!-- 아이콘2 -->
          <div class="bb_processIcon1">
            <!-- 아이콘2_이미지 -->
            <div class="bb_processIcon1_img">
              <img src="/public/images/yr/page1/1p_icon2.png" alt="icon2" />
            </div>
            <!-- 아이콘2_글 -->
            <span>사진촬영/업로드</span>
            <div class="bb_kakao">
              <div class="bb_kakaoIcon">
                <img src="/public/images/yr/page1/ktalk.png" alt="" />
              </div>
              <span class="bb_ktalkP">가방도</span>
            </div>
          </div>
          <!-- 화살표 -->
          <div class="arrow">
            <img src="/public/images/yr/page1/arrow.png" alt="arrow1" />
          </div>
          <!-- 아이콘3 -->
          <div class="bb_processIcon1">
            <!-- 아이콘3_이미지 -->
            <div class="bb_processIcon1_img">
              <img src="/public/images/yr/page1/1p_icon3.png" alt="icon3" />
            </div>
            <!-- 아이콘3_글 -->
            <span>픽업/배송</span>
          </div>
          <!-- 화살표 -->
          <div class="arrow">
            <img src="/public/images/yr/page1/arrow.png" alt="arrow1" />
          </div>
          <!-- 아이콘4 -->
          <div class="bb_processIcon1">
            <!-- 아이콘4_이미지 -->
            <div class="bb_processIcon1_img">
              <img src="/public/images/yr/page1/1p_icon4.png" alt="icon4" />
            </div>
            <!-- 아이콘4_글 -->
            <span>짐찾기</span>
          </div>
        </div>
        <!-- 예약하기 버튼 -->
        <div class="bb_reservation_btn"><button>예약하기</button></div>
      </div>
    </div>
    <!-- 전달방법 -->
    <div class="bb_container2">
      <div class="bb_inner">
        <!-- 타이틀 2 -->
        <div class="bb_title2">
          <!-- 제목 스타일 -->
          <div class="bb_titleLine"></div>
          <!-- 제목 -->
          <div class="bb_title_txt2">
            <h1>가방전달 방법</h1>
            <p>출발지별 안내사항</p>
          </div>
        </div>

        <!-- 전달방법 카드 3개 -->
        <div class="bb_cardAll">
          <!-- 카드1 -->
          <div class="bb_card">
            <div class="bb_card1">
              <!-- 카드1 왼쪽 -->
              <div class="bb_card1Left">
                <!-- 카드1 제목 -->
                <div class="bb_cardTitle">
                  <p>출발지가</p>
                  <h3>공항인 경우</h3>
                </div>
                <!-- 카드1 아이콘 -->
                <div class="bb_card1Icon">
                  <img
                    src="/public/images/yr/page1/1p_icon5.png"
                    alt="비행기" />
                </div>
              </div>
              <!-- 카드1 중간 -->
              <div class="bb_cardMiddle">
                <div class="bb_stepNumber"><p>1</p></div>
                <div class="bb_stepNumber1Line">
                  <!-- 숫자 회색라인 -->
                </div>
                <div class="bb_stepNumber"><p>2</p></div>
                <div class="bb_stepNumber1Line">
                  <!-- 숫자 회색라인 -->
                </div>
                <div class="bb_stepNumber"><p>3</p></div>
              </div>
              <!-- 카드1 오른쪽 -->
              <div class="bb_card1Right">
                <!-- 순서1 -->
                <div class="bb_card1Step1">
                  <div class="bb_cardTxt">
                    <p class="bb_stepTitle">예약된 픽업 시간 도착</p>
                    <p class="bb_stepContent">
                      고객이 설정한 픽업 시간에 운송 담당자가 지정된 장소로
                      도착하여 신분 확인 후 짐을 수거합니다.
                    </p>
                  </div>
                </div>
                <div class="bb_card1Step2">
                  <div class="bb_cardTxt">
                    <p class="bb_stepTitle">가방 전달</p>
                    <p class="bb_stepContent">
                      고객이 짐을 맡기면 태그가 부착되며, 취급 주의가 필요한
                      짐은 별도 라벨로 관리됩니다.
                    </p>
                  </div>
                </div>
                <div class="bb_card1Step3">
                  <div class="bb_cardTxt">
                    <p class="bb_stepTitle">확인 메시지 수신</p>
                    <p class="bb_stepContent">
                      운송 담당자가 짐을 수거하면 픽업 완료 및 예상 도착 시간이
                      포함된 메시지가 발송됩니다.
                    </p>
                  </div>
                </div>
              </div>
              <button class="bb_pickupBtn">픽업장소 위치안내</button>
            </div>
          </div>
          <!-- 카드2 -->
          <div class="bb_card">
            <div class="bb_card1">
              <!-- 카드2 왼쪽 -->
              <div class="bb_card1Left">
                <!-- 카드2 제목 -->
                <div class="bb_cardTitle">
                  <p>출발지가</p>
                  <h3>숙소인 경우</h3>
                </div>
                <!-- 카드2 아이콘 -->
                <div class="bb_card1Icon">
                  <img src="/public/images/yr/page1/1p_icon6.png" alt="숙소" />
                </div>
              </div>
              <!-- 카드2 중간 -->
              <div class="bb_cardMiddle">
                <div class="bb_stepNumber"><p>1</p></div>
                <div class="bb_stepNumber1Line">
                  <!-- 숫자 회색라인 -->
                </div>
                <div class="bb_stepNumber"><p>2</p></div>
                <div class="bb_stepNumber1Line">
                  <!-- 숫자 회색라인 -->
                </div>
                <div class="bb_stepNumber"><p>3</p></div>
              </div>
              <!-- 카드2 오른쪽 -->
              <div class="bb_card1Right">
                <!-- 순서1 -->
                <div class="bb_card1Step1">
                  <div class="bb_cardTxt">
                    <p class="bb_stepTitle">로비 / 프론트 데스크</p>
                    <p class="bb_stepContent">
                      고객이 프론트 데스크에 짐을 맡기면 숙소 직원이 운송
                      담당자에게 전달합니다.
                    </p>
                  </div>
                </div>
                <div class="bb_card1Step2">
                  <div class="bb_cardTxt">
                    <p class="bb_stepTitle">가방 전달</p>
                    <p class="bb_stepContent">
                      운송 담당자가 숙소에서 짐을 수거하여 태그를 부착하고
                      운송을 준비합니다.
                    </p>
                  </div>
                </div>
                <div class="bb_card1Step3">
                  <div class="bb_cardTxt">
                    <p class="bb_stepTitle">고객 직접 전달 가능</p>
                    <p class="bb_stepContent">
                      운송 담당자가 짐을 수거하면 픽업 완료 및 예상 도착 시간이
                      포함된 메시지가 발송됩니다.
                    </p>
                  </div>
                </div>
              </div>
              <button class="bb_pickupBtn">픽업장소 위치안내</button>
            </div>
          </div>
          <!-- 카드3 -->
          <div class="bb_card">
            <div class="bb_card1">
              <!-- 카드3 왼쪽 -->
              <div class="bb_card1Left">
                <!-- 카드3 제목 -->
                <div class="bb_cardTitle">
                  <p>출발지가</p>
                  <h3>기차역인 경우</h3>
                </div>
                <!-- 카드3 아이콘 -->
                <div class="bb_card1Icon">
                  <img
                    src="/public/images/yr/page1/1p_icon7.png"
                    alt="비행기" />
                </div>
              </div>
              <!-- 카드3 중간 -->
              <div class="bb_cardMiddle">
                <div class="bb_stepNumber"><p>1</p></div>
                <div class="bb_stepNumber1Line">
                  <!-- 숫자 회색라인 -->
                </div>
                <div class="bb_stepNumber"><p>2</p></div>
                <div class="bb_stepNumber1Line">
                  <!-- 숫자 회색라인 -->
                </div>
                <div class="bb_stepNumber"><p>3</p></div>
              </div>
              <!-- 카드3 오른쪽 -->
              <div class="bb_card1Right">
                <!-- 순서1 -->
                <div class="bb_card1Step1">
                  <div class="bb_cardTxt">
                    <p class="bb_stepTitle">지정된 출구 / 대기장소</p>
                    <p class="bb_stepContent">
                      고객은 사전에 안내된 기차 출구 또는 대기 장소에서 운송
                      담당자를 만납니다.
                    </p>
                  </div>
                </div>
                <div class="bb_card1Step2">
                  <div class="bb_cardTxt">
                    <p class="bb_stepTitle">가방 전달</p>
                    <p class="bb_stepContent">
                      고객이 짐을 맡기면 태그가 부착되며, 취급 주의가 필요한
                      짐은 별도 라벨로 관리됩니다.
                    </p>
                  </div>
                </div>
                <div class="bb_card1Step3">
                  <div class="bb_cardTxt">
                    <p class="bb_stepTitle">도착 후 직원 연락</p>
                    <p class="bb_stepContent">
                      운송 담당자가 짐을 수거하면 픽업 완료 및 예상 도착 시간이
                      포함된 메시지가 발송됩니다.
                    </p>
                  </div>
                </div>
              </div>
              <button class="bb_pickupBtn">픽업장소 위치안내</button>
            </div>
          </div>
        </div>
      </div>
      <!-- 유의사항1 -->

      <div class="bb_container3">
        <div class="bb_inner">
          <!-- 공지 왼쪽 -->
          <div class="bb_contain3Left">
            <!-- 용달씨 그림 -->
            <div class="bb_yongdal">
              <img src="/public/images/yr/page1/1p_character.png" alt="" />
            </div>
            <p>확인해주세요!</p>
          </div>

          <!-- 공지 오른쪽 -->
          <div class="bb_contain3Right">
            <!-- 유의사항_위 -->
            <div class="bb_noteTop">
              <ul class="bb_notice1">
                <li>• 서비스 이용 전에 반드시 예약을 진행해 주세요.</li>
                <li>
                  • 출발지로부터 30km 이내에 있는 장소로만 배송할 수 있습니다.
                </li>
                <li>
                  • 직접 투숙하는 숙소에서만 짐을 맡기고 찾으실 수 있습니다.
                </li>
                <li>
                  • 짐을 맡기고 찾는 시간은 장소별로 정해진 시간 내에서만
                  선택하실 수 있습니다.
                </li>
                <li>
                  • 한 번 예약한 뒤에는 배송지 변경이 어려우니 예약하실 때
                  출발지와 도착지를 정확히 확인해 주세요.
                </li>
                <li>
                  • 안전한 배송을 위해 맡기는 짐의 사진을 꼭 촬영하고 업로드
                  해주세요.
                </li>
              </ul>
            </div>
            <!-- 유의사항_아래 -->
            <div class="bb_noteDown">
              <h2 class="bb_noticeSubtitle">불가물품 및 기타물품</h2>
              <ul class="bb_notice2">
                <li>• 비닐/종이 쇼핑백, 우산, 박스 등 파손 위험이 있는 물품</li>
                <li>• 부패성 및 악취가 심한 물품</li>
                <li>• 타인에게 해를 가할 수 있는 물품</li>
                <li>• 일반 위탁수하물 허용량을 초과한 물품</li>
              </ul>
            </div>
          </div>
        </div>
      </div>

      <!-- 유의사항2 -->
      <div class="bb_container4">
        <div class="bb_innerBottom">
          <div class="bb_title3">
            <!-- 제목 스타일 -->
            <div class="bb_titleLine"></div>
            <!-- 제목 -->
            <div class="bb_title_txt3">
              <h1>가방분실 / 파손시 유의사항</h1>
            </div>
          </div>
        </div>
        <div class="bb_container4Bg">
          <div class="bb_inner">
            <!-- 타이틀3 -->

            <!-- 유의사항 긴글 -->
            <div class="bb_notice">
              <h3>기본 보상 제공</h3>
              <p>
                서비스 이용 중 가방이 분실되거나 심각한 손상이 발생한 경우, 최대
                30만 원까지 보상됩니다.
              </p>
              <h3>추가 보장 옵션 (선택 사항)</h3>
              <p>
                고객이 추가 보험 옵션을 선택할 경우, 기본 보상 외 추가 금액 보장
                가능 (상세 조건은 보험 상품에 따라 다름).
              </p>
              <h3>보험 적용 제외 사항</h3>
              <ul>
                <li>• 고객의 부주의로 인해 발생한 분실 또는 손상</li>
                <li>
                  • 가방 내부 물품의 파손, 분실 (가방 자체가 아닌 내용물 손상은
                  보상 불가)
                </li>
              </ul>

              <h3  class="_bbTum">안전한 운송 시스템</h3>
              <p>
                모든 가방은 철저하게 관리되며, 실시간 추적을 통해 더욱 안전하게
                보관 및 배송됩니다.
              </p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup></script>

<style lang="scss" scoped>
@use "/src/assets/_Variables.scss" as *;
.bb_wrap {
  position: relative;
  padding-top: 100px;
  // 이너
  .bb_inner {
    position: relative;
    max-width: 1300px;
    margin: 0 auto;
    // background-color: beige;

    // 컨테이너1
    .bb_container1 {
      position: relative;
      width: 100%;
      // background-color: bisque;
      text-align: center;
      // 타이틀
      .bb_title1 {
        display: flex;
        gap: 10px;
        line-height: 40px;
        flex-wrap: wrap; /* 넘치면 자동 줄바꿈 */
        align-items: center; /* 세로 중앙 정렬 */
        justify-content: center; /* 가로 중앙 정렬 */
        padding-bottom: 10px;
        .bb_titleLine {
          width: 3px;
          height: 35px;
          background-color: $main-color;
        }
        .title_txt1 h1 {
          font-size: 30px;
        }
      }
      // 이용절차
      .bb_orderProcess {
        position: relative;
        // background-color: aqua;
        width: 100%;
        display: flex;
        flex-wrap: wrap;
        justify-content: space-between;
        .bb_processIcon1 {
          text-align: center;
          position: relative;
          .bb_processIcon1_img {
            position: relative;
            width: 90%;
            // background-color: rebeccapurple;
          }
        }
        span {
          font-size: 25px;
        }
        .arrow {
          position: relative;
          padding: 90px 0 120px 0;
          .img {
            position: relative;
            top: 0;
            width: 40%;
            height: 40%;
          }
        }
        .bb_processIcon1 {
          display: flex;
          flex-direction: column;
          align-items: center;
          .bb_kakao {
            display: flex;
            background-color: #f4f4f4;
            border-radius: 80px;
            width: 45%;
            position: relative;
            margin-top: 20px;
            cursor: pointer;
            .bb_kakaoIcon {
              padding: 3px;

              img {
                border-radius: 50px;
                width: 30px;
                height: 30px;
              }
            }

            .bb_ktalkP {
              position: relative;
              text-align: center;
              margin-top: 6.5px;
              padding-left: 3px;
              font-size: 20px;
            }
          }
        }
      }
      .bb_reservation_btn button {
        background-color: $main-color;
        color: $notice-1stcolor;
        border-radius: 40px;
        padding: 1% 4% 1% 4%;
        font-size: 25px;
        white-space: nowrap;
        border: none;
        margin-top: 4%;
        margin-bottom: 6%;
        cursor: pointer;
      }
    }
  }
  .bb_container2 {
    background-color: $background-maincolor;
    width: 100%;
    .bb_title2 {
      padding-top: 6%;
      display: flex;
      gap: 10px;
      line-height: 40px;
      padding-bottom: 4%;
      .bb_titleLine {
        width: 3px;
        height: 35px;
        background-color: $main-color;
      }
      .bb_title_txt2 h1 {
        font-size: 30px;
      }
      .bb_title_txt2 p {
        font-size: 20px;
      }
    }
    // 전달방법 카드전체
    .bb_cardAll {
      padding-bottom: 10%;
      .bb_card {
        padding-top: 3%;
        position: relative;
        width: 100%;
        height: 50%;
        padding-left: 30px;
        background-color: rgb(255, 255, 255);
        border: $main-color solid 1.8px;
        border-radius: 30px;
        margin-bottom: 2%;
        // 전달방법 카드1
        .bb_card1 {
          width: 100%;
          display: flex;
          // 카드 왼쪽
          .bb_card1Left {
            position: relative;
            .bb_cardTitle {
              // padding-top: 20px;
              padding-left: 50px;
              padding-top: 20px;
              p {
                font-size: 15px;
                font-weight: bold;
                color: #ababab;
                margin-bottom: 10px;
              }
              h3 {
                font-size: 25px;
                color: $main-color;
                font-weight: bold;
              }
            }
            .bb_card1Icon {
              position: relative;
              padding-left: 22px;
              padding-top: 30px;

              // background-color: rebeccapurple;
              width: 90%;
              img {
                width: 100%;
              }
            }
          }
          // 카드중간
          .bb_cardMiddle {
            padding-top: 70px;
            padding-left: 30px;
            .bb_stepNumber {
              width: 15px;
              background-color: $main-color;
              border-radius: 200px;
              padding: 4px 16px 4px 16px;
              display: flex;
              justify-content: center; /* 가로 중앙 */
              align-items: center; /* 세로 중앙 */
              p {
                font-size: 25px;
                color: #fff;
              }
            }
            .bb_stepNumber1Line {
              background-color: #d8d8d8;
              width: 7px;
              height: 70px;
              margin-left: 12px;
            }
          }
          // 카드 오른쪽
          .bb_card1Right {
            padding-left: 40px;
            padding-top: 75px;
            // 카드 순서1
            .bb_card1Step1 {
              display: flex;
              .bb_cardTxt {
                .bb_stepTitle {
                  font-size: 23px;
                  color: $main-color;
                  font-weight: bold;
                }
                .bb_stepContent {
                  font-size: 15px;
                  color: #ababab;
                  padding-top: 13px;
                }
              }
            }

            // 카드 순서2
            .bb_card1Step2 {
              display: flex;

              .bb_cardTxt {
                padding-top: 53px;
                .bb_stepTitle {
                  font-size: 23px;
                  color: $main-color;
                  font-weight: bold;
                  color: #00b3eb;
                }
                .bb_stepContent {
                  font-size: 15px;
                  color: #ababab;
                  padding-top: 13px;
                }
              }
            }
            // 카드 순서3
            .bb_card1Step3 {
              display: flex;
              .bb_cardTxt {
                padding-top: 50px;
                .bb_stepTitle {
                  font-size: 23px;
                  color: $main-color;
                  font-weight: bold;
                }
                .bb_stepContent {
                  font-size: 15px;
                  color: #ababab;
                  padding-top: 13px;
                }
              }
            }
          }
          .bb_pickupBtn {
            position: relative;
            background-color: $main-color;
            color: $notice-1stcolor;
            border-radius: 13px;
            padding: 5px 12px 5px 12px;
            font-size: 15px;
            font-weight: bold;
            height: 10%;
            border: none;
            cursor: pointer;
            margin-top: 370px;
            margin-bottom: 20px;
            margin-left: 190px;
          }
        }
      }
    }
  }
  // 유의사항1
  .bb_container3 {
    padding-top: 70px;
    padding-bottom: 70px;
    padding-left: 15%;
    position: relative;
    width: 100%;
    background-color: #fff;
    .bb_inner {
      position: relative;
      max-width: 1300px;
      margin: 0 auto;
      display: flex;
      // 유의사항 왼쪽
      .bb_contain3Left {
        display: flex;
        flex-direction: column;
        align-items: center;
        .bb_yongdal {
          width: 80%;
          img {
            width: 100%;
          }
        }
        p {
          font-size: 20px;
          font-weight: bold;
        }
      }
      // 유의사항 오른쪽
      .bb_contain3Right {
        .bb_noteTop {
          .bb_notice1 {
            li {
              line-height: 22px;
              font-size: 15px;
            }
          }
        }
        .bb_noteDown {
          width: 100%;
          margin-top: 4%;
          background-color: #ffcccc;
          border-radius: 10px;
          border: #f60000 1px solid;
          padding: 2% 2% 2% 2%;
          .bb_noticeSubtitle {
            font-size: 17px;
            font-weight: bold;
            padding-bottom: 10px;
          }

          .bb_notice2 {
            li {
              line-height: 22px;
              font-size: 15px;
            }
          }
        }
      }
    }
  }
  // 유의사항2
  .bb_container4 {
    background-color: #fff;
    padding-bottom: 60px;
    .bb_innerBottom {
      max-width: 1300px;
      margin: 0 auto;
      .bb_title3 {
        display: flex;
        gap: 10px;
        line-height: 40px;
        padding-bottom: 20px;
        .bb_titleLine {
          width: 3px;
          height: 35px;
          background-color: $main-color;
        }
        .bb_title_txt3 {
          font-size: 30px;
        }
      }
    }
    .bb_container4Bg {
      background-color: #e9e9e9;
      .bb_inner {
        .bb_notice {
          padding-top: 2%;
          padding-bottom: 2%;
          h3 {
            font-size: 22px;
            padding-bottom: 5px;
          }
          p {
            padding-bottom: 20px;
          }
          li {
            padding-bottom: 5px;
          }
          ._bbTum{
            padding-top: 10px;
          }
        }
      }
    }
  }
}
</style>
