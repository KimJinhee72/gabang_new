<template>
  <div class="yy_wrap">
    <p class="yy_header">예약조회</p>

    <div class="yy_check" v-if="selectedReservation">
      <div class="reservation-item">
        <table class="reservation-table">
          <tbody>
            <tr>
              <th>이름 :</th>
              <td>{{ selectedReservation.name }}</td>
            </tr>
            <tr>
              <th>날짜 :</th>
              <td>{{ selectedReservation.date }}</td>
            </tr>
            <tr>
              <th>시간 :</th>
              <td>{{ selectedReservation.time }}</td>
            </tr>
            <tr>
              <th>출발 :</th>
              <td>{{ selectedReservation.start }}</td>
            </tr>
            <tr>
              <th>도착 :</th>
              <td>{{ selectedReservation.stop }}</td>
            </tr>
            <tr>
              <th>가방 수량 :</th>
              <td>
                <p v-for="(bag, i) in selectedReservation.bags" :key="i">
                  {{ bag.label }} 사이즈 ({{ bag.count }}개)
                </p>
              </td>
            </tr>
          </tbody>
        </table>
      </div>
    </div>
    <router-link to="/"><button>처음으로</button></router-link>
  </div>
</template>
<script setup>
import { ref, onMounted } from "vue";

const reservations = ref([]);
const selectedReservation = ref(null);

const names = ["김철수", "이영희", "박지민", "최준호", "장서연"];
const places = ["공항", "동대구역", "숙소", "기타"];
const bagTypes = ["S", "M", "L", "기타"];

function getRandomItem(arr) {
  return arr[Math.floor(Math.random() * arr.length)];
}

function getRandomInt(min, max) {
  return Math.floor(Math.random() * (max - min + 1)) + min;
}

function generateRandomDate() {
  const today = new Date();
  const randomOffset = Math.floor(Math.random() * 7);
  const newDate = new Date(today.setDate(today.getDate() + randomOffset));
  return newDate.toISOString().split("T")[0];
}

function generateRandomBags() {
  return bagTypes
    .map((type) => ({
      label: type,
      count: getRandomInt(0, 3), // 0~3개 랜덤
    }))
    .filter((bag) => bag.count > 0);
}

function generateDummyReservations(count = 5) {
  const result = [];
  for (let i = 0; i < count; i++) {
    result.push({
      name: getRandomItem(names),
      date: generateRandomDate(),
      time: `${String(getRandomInt(0, 23)).padStart(2, "0")}:${String(
        getRandomInt(0, 59)
      ).padStart(2, "0")}`,
      start: getRandomItem(places),
      stop: getRandomItem(places),
      bags: generateRandomBags(),
    });
  }
  return result;
}

onMounted(() => {
  const dummy = generateDummyReservations(5); // 전체 생성
  reservations.value = dummy;
  selectedReservation.value = getRandomItem(dummy); // 하나만 랜덤 선택
});
</script>
<style lang="scss" scoped>
@use "@/assets/Main.scss" as *;
@use "@/assets/_Variables.scss" as *;

.yy_wrap {
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

.yy_header {
  text-align: center;
  font-size: $title-font-size-s;
  margin-bottom: $margin-m;
  padding-left: $padding-sss;
  border-left: 5px solid $main-color;
}
.yy_check {
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
.reservation-table {
  width: 100%;
  max-width: 600px;
  border-collapse: collapse;
  margin: 20px auto;
}

.reservation-table th,
.reservation-table td {
  padding: 10px;
  text-align: left;
  vertical-align: top;
}

.reservation-table th {
  width: 100px;
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
