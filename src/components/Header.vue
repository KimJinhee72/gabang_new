<template>
  <header>
    <div class="header">
      <div class="inner">
        <div class="hd_wideMenu">
          <router-link to="/" class="hd_logo"
            ><img src="/images/txtlogo.png" alt="로고"
          /></router-link>
          <nav v-if="!isMobile" class="hd_menu">
            <ul>
              <li v-for="(item, index) in menuItems" :key="index" @mouseenter="openedMenu = index">
                <router-link
                  v-if="!item.sub"
                  :to="item.to"
                  :class="{ mainMenu: item.label === '예약도' }"
                  ><span>{{ item.label }}</span></router-link
                >
                <a
                  v-else
                  href="#"
                  :class="{ mainMenu: item.label === '예약도' }">
                  {{ item.label }}
                </a>
                <ul
                  v-if="item.sub"
                  @mouseleave="closeSubMenu"
                  class="subMenu"
                  :class="{ show: openedMenu === index }">
                  <li v-for="(sub, idx) in item.sub" :key="idx">
                    <router-link :to="sub.to">{{ sub.label }}</router-link>
                  </li>
                </ul>
              </li>
            </ul>
          </nav>
          <nav class="hd_extra">
            <router-link to="/delivery">가방조회</router-link> |
            <div class="hd_myPage">
              <router-link to="/login" v-if="!isLoggedIn">로그인</router-link>
              <div class="hd_afterlogindropPage" v-else>
                <span class="user-name">{{ userName }}</span>
                <div class="hd_afterlogindropPage_content">
                  <router-link to="/yeyak4">마이페이지</router-link>
                  <a @click="logout"> 로그아웃</a>
                </div>
              </div>
            </div>
          </nav>
        </div>
        <div class="hd_mobileMenu">
          <nav class="hd_extra1">
            <a href="#" class="hd_hambar" @click.prevent="showShortMenu"
              ><img src="/images/geen/bar_humburger_icon.png" alt="햄버거메뉴"
            /></a>
            <router-link to="/" class="hd_logo"
              ><img src="/images/txtlogo.png" alt="로고"
            /></router-link>
            <div class="hd_mobileRight">
              <router-link to="/delivery" class="hd_bag"
                ><img src="/images/bagfind_icon.png" alt="가방조회이미지"
              /></router-link>
              <router-link to="/login" class="hd_man"
                ><img src="/images/gh/man1_icon.png" alt="로그인이미지"
              /></router-link>
            </div>
          </nav>
        </div>
        <nav class="hd_menu1" :class="{ show: shortMenu }" v-show="shortMenu">
          <span @click.prevent="shortMenu = false" role="button">X</span>
          <router-link to="/bangbeob">방 법 도</router-link>
          <router-link to="/yeyak">예 약 도</router-link>
          <router-link to="/yogeum">요 금 도</router-link>
          <router-link to="/sotong">소 통 도</router-link>
          <router-link to="/yeohaeng">여 행 도</router-link>
        </nav>
      </div>
    </div>
  </header>
</template>

<script setup>
import { ref, onMounted, onUnmounted, watch } from "vue";
import { useRouter } from "vue-router";
import { useAuthStore } from "../stores/auth";
import { storeToRefs } from "pinia";

// 모바일 여부 체크용
const isMobile = ref(window.innerWidth < 896);
//
const router = useRouter();
const authStore = useAuthStore();
const { isLoggedIn, userName } = storeToRefs(authStore);
const logout = () => {
  authStore.logout();
  router.push("/");
};
// 메뉴 호버
const openedMenu = ref(null); // 현재 열린 서브메뉴 li의 index
const menuItems = [
  {
    label: "방법도",
    sub: [
      { label: "짐 운송", to: "/bangbeob" },
      { label: "짐 보관", to: "/bangbeob1" },
    ],
  },
  {
    label: "요금도",
    to: "/yogeum",
  },
  {
    label: "예약도",
    sub: [
      { label: "예약하기", to: "/yeyak" },
      { label: "예약조회", to: "/yeyaklookup" },
    ],
  },
  {
    label: "소통도",
    sub: [
      { label: "공지사항", to: "/sotong" },
      { label: "이용후기", to: "/sotong2" },
    ],
  },
  {
    label: "여행도",
    sub: [
      { label: "대구축제", to: "/yh_festival" },
      { label: "시티투어", to: "/yeohaeng" },
    ],
  },
];
const closeSubMenu = () => {
  console.log('mouseleave 발생!');
  openedMenu.value = null;
};

// 햄버거 메뉴 토글 상태
const shortMenu = ref(false);

// 햄버거 아이콘 클릭 시 메뉴 토글
const showShortMenu = () => {
  shortMenu.value = !shortMenu.value;
};
// 햄버거 메뉴 열릴 때 body 스크롤 방지
watch(shortMenu, (val) => {
  document.body.style.overflow = val ? "hidden" : "auto";
});

// 창 크기 변경 시 모바일 여부 확인 + 창이 커지면 메뉴 닫기
const updateScreenSize = () => {
  const width = window.innerWidth;
  isMobile.value = width <= 896;

  // 화면이 896 이상이면 메뉴 강제 닫기
  if (width > 896) {
    shortMenu.value = false;
  }
};

// 이벤트 리스너 등록
onMounted(() => {
  window.addEventListener("resize", updateScreenSize);
  updateScreenSize(); // 최초 진입 시 확인
});

// 이벤트 리스너 해제
onUnmounted(() => {
  window.removeEventListener("resize", updateScreenSize);
});
</script>

<style lang="scss" scoped>
@use "/src/assets/Variables" as *;
.header {
  position: fixed;
  top: 0;
  left: 50%;
  transform: translateX(-50%);
  width: 100%;
  height: 75px;
  padding-top: 13px;
  z-index: 1;
  background-color: #fff;
  box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
}
header .inner {
  max-width: 1300px;
  margin-top: 5px;
  margin: auto;
  display: flex;
  justify-content: space-between;
  align-items: center;
}
.hd_wideMenu {
  width: 100%;
  height: 100%;
  display: flex;
  justify-content: space-between;
}
// 로고
.hd_logo {
  width: 140px;
  img {
    width: 120px;
  }
}
.hd_mobileMenu {
  width: 100%;
  display: none;
}

// 메뉴
.hd_menu {
  width: 700px;
  margin-top: 7px;
  display: flex;
  justify-content: space-evenly;
  align-items: center;
  ul {
    display: flex;
    width: 100%;
    height: 100%;
    li {
      position: relative;
      flex: 1;
      text-align: center;
      &:hover .subMenu {
        display: flex; // hover 중에는 항상 보이게
      }

      a {
        display: inline-block;
        padding: 10px 15px;
        transition: all 0.3s ease;
        border-radius: 5px;
        font-weight: normal;
      }

      a:hover {
        color: #fff;
        font-weight: bold;
        background-color: $main-color;
      }
      .mainMenu {
        border: 1px solid $main-color;
      }
      .subMenu {
        width: 100%;
        height: 100px;
        display: none;
        flex-direction: column;
        position: absolute;
        top: 57px;
        left: 0;
        background-color: #fff;
        box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
        z-index: 10;
        padding: 10px 0;
      }
      .subMenu.show {
        display: flex;
      }
    }
  }
}
.hd_menu1 {
  pointer-events: none;
  position: fixed;
  top: 75px;
  right: 200px;
  width: 230px;
  height: calc(60px * 6 + 20px);
  display: flex;
  flex-direction: column;
  font-size: 20px;
  border-radius: 10px;
  transition: all 0.3s ease;
  opacity: 0;
  background-color: rgba($main-color, 0.8);
}
.hd_menu1.show {
  height: 380px;
  text-align: right;
  color: #fff;
  cursor: pointer;
  opacity: 1;
  transform: translateY(0);
  pointer-events: auto;
}
.hd_menu1 span {
  height: 50px;
  text-align: right;
  color: #fff;
  cursor: pointer;
}
.hd_menu1 > a {
  width: 95%;
  height: 60px;
  padding: 18px 10px;
  color: #fff;
  text-align: center;
  box-sizing: border-box;
  border-radius: 10px;
  border: 2.5px solid #0066b333;
}
.hd_menu1 a:hover {
  border: 2.5px solid $sub-color;
  font-weight: bold;
  border-radius: 10px;
}
.hd_menu1 a:last-child {
  margin-bottom: 20px;
}
// delivery/login icon
.hd_extra {
  width: 17%;
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 5px;
  color: $main-color;
  img {
    width: 40px;
    font-weight: 600;
    filter: invert(31%) sepia(97%) saturate(400%) hue-rotate(169deg)
      brightness(95%) contrast(96%);
  }
}
.hd_extra > div > a {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 100%;
  text-align: center;
  border: 1px solid transparent;
}
// 로그인
.hd_myPage {
  position: relative;
}

.hd_afterlogindropPage_content {
  display: none;
  position: absolute;
  right: 0;
  background-color: #fff;
  min-width: 160px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  border-radius: 4px;
  padding: 0.5rem 0;
}

.hd_afterlogindropPage:hover .hd_afterlogindropPage_content {
  display: block;
}

.hd_afterlogindropPage_content a {
  display: block;
  padding: 0.5rem 1rem;
  color: #333;
  text-decoration: none;
}

.hd_afterlogindropPage_content a:hover {
  background-color: #f5f5f5;
}
.user-name {
  color: $main-color;
}
// 반응형후 delivery/login icon
.hd_extra1 {
  width: 100% !important;
  display: flex;
  justify-content: space-around;
  align-items: center;
  img {
    font-weight: 600;
  }
}
.hd_hambar,
.hd_hambar > img {
  width: 30px;
  filter: invert(31%) sepia(97%) saturate(800%) hue-rotate(169deg)
    brightness(60%) contrast(96%);
}
.hd_bag img {
  filter: invert(31%) sepia(97%) saturate(400%) hue-rotate(169deg)
    brightness(105%) contrast(96%);
}
.hd_man,
.hd_man img {
  width: 32px;
  height: 33px;
  filter: invert(31%) sepia(97%) saturate(800%) hue-rotate(169deg)
    brightness(60%) contrast(96%);
}
.hd_mobileRight {
  width: 12%;
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 10px;
}
</style>
