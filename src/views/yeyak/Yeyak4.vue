<script setup>
import { useReservationStore } from "../../stores/reservationStore";
import { ref } from "vue";

const selectedPayment = ref("");
const reservationStore = useReservationStore();
</script>

<template>
  <div class="st_wrap">
    <div class="yy_title1">
      <!-- 제목 스타일 -->
      <div class="yy_titleLine"></div>
      <!-- 제목 -->
      <div class="title_txt1">
        <h1>예약확인</h1>
      </div>
    </div>
    <div class="st_check">
      <table class="st_table">
        <tbody>
          <tr>
            <th>이름 :</th>
            <td>{{ reservationStore.name }}</td>
          </tr>
          <tr>
            <th>전화번호 :</th>
            <td>{{ reservationStore.phone }}</td>
          </tr>
          <tr>
            <th>날짜 :</th>
            <td>{{ reservationStore.selectedDate }}</td>
          </tr>
          <tr>
            <th>시간 :</th>
            <td>
              {{ reservationStore.selectedHour }}시
              {{ reservationStore.selectedMinute }}분
            </td>
          </tr>
          <tr>
            <th>출발 :</th>
            <td>{{ reservationStore.selectedStart }}</td>
          </tr>
          <tr>
            <th>도착 :</th>
            <td>{{ reservationStore.selectedStop }}</td>
          </tr>
          <tr>
            <th rowspan="{{ reservationStore.sizes.length }}">가방수량 :</th>
            <td>
              <p v-for="(item, i) in reservationStore.sizes" :key="i">
                {{ item.label }} ({{ item.count }}개)
              </p>
            </td>
          </tr>
          <tr>
            <th>총 금액 :</th>
            <td>{{ reservationStore.totalPrice.toLocaleString() }}원</td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="yy_credit">
      <label class="credit-option">
        <input type="radio" value="bank" v-model="selectedPayment" />
        <span>계좌이체</span>
      </label>
      <label class="credit-option">
        <input type="radio" value="card" v-model="selectedPayment" />
        <span>카드결제</span>
      </label>
    </div>

    <div v-if="selectedPayment === 'bank'" class="payment-info">
      <h4>계좌이체</h4>
      <p>대구은행 123-456-78910 예금주: 도용달</p>
    </div>

    <div v-if="selectedPayment === 'card'" class="payment-info">
      <h4>카드결제</h4>
      <p>신용카드 결제는 다음 단계에서 진행됩니다.</p>
    </div>
    <router-link to="/"><button>처음으로</button></router-link>
  </div>
</template>
<style lang="scss" scoped>
@use "@/assets/Main.scss" as *;
@use "@/assets/_Variables.scss" as *;

.st_wrap {
  width: 100%;
  max-width: 700px;
  margin: 100px auto;
  display: flex;
  flex-direction: column;
  align-items: center;
  font-family: $font-family;
}
.yy_title1 {
  display: flex;
  gap: 10px;
  line-height: 40px;
  flex-wrap: wrap; /* 넘치면 자동 줄바꿈 */
  align-items: center; /* 세로 중앙 정렬 */
  justify-content: center; /* 가로 중앙 정렬 */
  padding-bottom: 10px;
  .yy_titleLine {
    width: 3px;
    height: 25px;
    background-color: $main-color;
  }
  .title_txt1 h1 {
    font-size: 25px;
  }
}
.st_check {
  width: 100%;
  padding: 20px;
  background-color: #a3e4ff;
  border-radius: 20px;

  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}
.st_table {
  width: 50%;
  border-collapse: collapse;
  margin: 20px auto;

  th,
  td {
    padding: 10px;
    text-align: left;
    vertical-align: top;
  }
  th {
    width: 100px;
    text-align: left;
    white-space: nowrap;
  }
}
.yy_credit {
  display: flex;
  gap: 1rem;
  margin-bottom: 1rem;
}
.credit-option {
  display: flex;
  align-items: center;
  gap: 0.5rem;
  cursor: pointer;
}
.payment-info {
  padding: 1rem;
  background: #f5f5f5;
  border-radius: 8px;
  border: 1px solid #ddd;
  transition: all 0.3s ease;
}

.credit-option {
  display: flex;
  align-items: center;
  padding: 0.75rem 1.25rem;
  border: 2px solid #ccc;
  border-radius: 10px;
  cursor: pointer;
  transition: all 0.2s ease-in-out;
  font-size: 16px;
  background-color: #f9f9f9;
}

.credit-option:hover {
  border-color: #007bff;
}

.credit-option input[type="radio"] {
  display: none;
}

.credit-option span {
  position: relative;
  padding-left: 24px;
}

.credit-option span::before {
  content: "";
  position: absolute;
  left: 0;
  top: 4px;
  width: 16px;
  height: 16px;
  border: 2px solid #aaa;
  border-radius: 50%;
  background-color: #fff;
}

.credit-option input[type="radio"]:checked + span::before {
  border-color: #007bff;
  background-color: #007bff;
}

.credit-option input[type="radio"]:checked + span {
  font-weight: bold;
  color: #007bff;
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
@media (max-width: 390px) {
  .st_wrap {
    margin: 50px auto;
    padding: 0 16px;
  }

  .st_table {
    width: 100%;
    font-size: 14px;
    th,
    td {
      padding: 6px;
    }
  }

  .yy_credit {
    flex-direction: column;
    gap: 0.5rem;
    align-items: stretch;
  }

  .credit-option {
    width: 100%;
    font-size: 15px;
    padding: 0.75rem;
    justify-content: flex-start;
  }

  .payment-info {
    font-size: 14px;
    padding: 0.75rem;
  }

  .title_txt1 h1 {
    font-size: 20px;
  }

  button {
    width: 100%;
    font-size: 16px;
    padding: 0.75rem;
  }
}
</style>
