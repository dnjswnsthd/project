<template>
  <header>
    <v-row class="headerBox">
      <v-col @click="goStart" class="logo">
        <img :src="logo" alt="로고" />
      </v-col>
      <v-spacer></v-spacer>
      <v-col @click="goBitCoinTrade" class="menuList">
        <img :src="trade" alt="거래소" class="menuImg" />
      </v-col>
      <v-spacer></v-spacer>
      <v-col @click="goSignUp" class="menuList">
        <img :src="signup" alt="회원가입" class="menuImg" />
      </v-col>
      <v-col class="menuList" @click="goLogin()">
        <img :src="login" alt="로그인" class="menuImg" />
      </v-col>
    </v-row>
  </header>
</template>

<script>
import {
  moveStart,
  moveLogin,
  moveSignUp,
  moveBitCoinTrade,
} from "@/api/move.js";
export default {
  name: "SubHeader",
  data() {
    return {
      logo: require("@/assets/images/header/logo.png"),
      signup: require("@/assets/images/header/sign-up.png"),
      login: require("@/assets/images/header/login.png"),
      trade: require("@/assets/images/header/trade.png"),
    };
  },
  methods: {
    goStart() {
      // 시작 페이지로 이동
      moveStart();
    },
    goSignUp() {
      // 회원가입 페이지로 이동
      moveSignUp();
    },
    goLogin() {
      // 로그인 페이지로 이동
      moveLogin();
    },
    goBitCoinTrade() {
      // 거래소 페이지로 이동
      moveBitCoinTrade();
    },
  },
};
</script>
<style scoped>
@import "./../../assets/css/header.css";
</style>
