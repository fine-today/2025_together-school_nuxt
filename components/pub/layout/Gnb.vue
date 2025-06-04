<template>
  <div class="gnb">
    <div class="wrap">
      <div class="color-mode" :class="colorMode ? 'bright' : 'dark'">
        <div class="input">
          <input type="checkbox" id="color-mode" v-model="colorMode" />
          <label for="color-mode">
            <Icons icon="modeDark" class="bright-icon" />
            <Icons icon="modeBright" class="dark-icon" />
            <span class="circle"></span>
            {{ colorMode ? "기본 컬러 모드" : "다크모드" }}</label
          >
        </div>
      </div>

      <div class="gnb-options">
        <span class="zoom-option">
          <span class="zoom-title"> 글자·화면 표시</span>
          <button type="button" class="zoom-btn reduce">
            화면 축소하기<Icons icon="reduce" />
          </button>
          <button type="button" class="zoom-btn expand">
            화면 확대하기 화면 축소하기<Icons icon="expand" />
          </button>
        </span>
        <button href="#n" class="braille-btn braille-down">
          전자점자다운로드 화면 축소하기<Icons icon="brailleDown" />
        </button>
        <button type="button" class="braille-btn braille-viewer">
          전자점자뷰어보기(새창열림)<Icons icon="brailleViewer" />
        </button>
      </div>
    </div>
  </div>
  <div class="lnb">
    <div class="wrap">
      <h1 class="logo">
        <a href="#n" class="logo-anchor">
          <Icons icon="logo" />
        </a>
      </h1>

      <div class="search">
        <span class="input">
          <input type="text" placeholder="검색어를 입력하세요" />
          <span class="search-btns">
            <button type="button" class="voice-btn">
              <Icons icon="voice" />
            </button>
            <button type="button" class="search-btn">
              <Icons icon="search" /></button
          ></span>
        </span>
      </div>

      <ul class="login-box">
        <li class="login-item">
          <a href="#n" class="login-anchor">
            <Icons icon="login" />
            <span class="title">로그인</span>
          </a>
        </li>
        <!--<li class="login-item">
          <a href="#n" class="login-anchor">
            <Icons icon="logout" />
            <span class="title">로그아웃</span>
          </a>
        </li>-->
        <li class="login-item">
          <a href="#n" class="login-anchor">
            <Icons icon="join" />
            <span class="title">회원가입</span>
          </a>
        </li>
        <li class="login-item">
          <a href="#n" class="login-anchor">
            <Icons icon="language" />
            <span class="title">언어선택</span>
          </a>
        </li>
      </ul>
    </div>
  </div>
</template>

<script setup>
import { ref } from "vue";
import Icons from "/components/pub/ui/Icons.vue";
const colorMode = ref(true);
</script>

<style></style>
