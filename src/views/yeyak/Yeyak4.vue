<script setup>
import { useReservationStore } from "@/views/yeyak/reservationStore.js";

const reservationStore = useReservationStore();
</script>

<template>
  <div class="st_wrap">
    <p class="st_header">예약확인</p>
    <div class="st_check">
      <table class="st_table">
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
          <th rowspan="reservationStore.sizes.length + 1">가방수량 :</th>
          <td>
            <p v-for="(item, i) in reservationStore.sizes" :key="i">
              {{ item.label }} ({{ item.count }}개)
            </p>
          </td>
        </tr>
      </table>
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
  margin: 0 auto $margin-m auto;
  padding-top: $margin-titletopbottom;
  display: flex;
  flex-direction: column;
  align-items: center;
  font-family: $font-family;
}
.st_header {
  font-size: $title-font-size-s;
  margin-bottom: $margin-m;
  padding-left: $padding-sss;
  border-left: 5px solid $main-color;
}
.st_check {
  width: 100%;
  padding: 20px;
  background-color: $background-maincolor;
  border-radius: 20px;
  box-shadow: 0 0 6px rgba(0, 0, 0, 0.1);
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
