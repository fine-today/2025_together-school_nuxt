<template>
  <div class="gnb">
    <div class="wrap">
      <div class="log">
        <div class="log-item">
          <span class="title">누적 방문자수</span>
          <span class="con"><b>3,656,128</b>명</span>
        </div>
        <div class="log-item">
          <span class="title">일 평균 방문자수</span>
          <span class="con"><b>5,966</b>명</span>
        </div>
        <div class="log-item">
          <span class="title">회원수</span>
          <span class="con"><b>154,834</b>명</span>
        </div>
      </div>

      <div class="login-box">
        <div class="login-item">
          <a href="#n" class="login-anchor login">로그인</a>
        </div>
        <div class="login-item">
          <a href="#n" class="login-anchor join">회원가입</a>
        </div>
        <div class="login-item">
          <a href="#n" class="login-anchor btn">함께학교 지식샘터</a>
        </div>
      </div>
    </div>
  </div>

  <!--================ menu-box ================-->
  <div class="menu-box">
    <div class="wrap">
      <button type="button" class="menu-btn">전체메뉴</button>
      <h1 class="logo">
        <a href="/">함께학교</a>
      </h1>

      <div class="btn-wrap">
        <!--================ search-wrap ================-->
        <div class="search-wrap">
          <form action="./">
            <fieldset>
              <legend>검색하기</legend>
              <div class="input-wrap">
                <div class="input">
                  <input type="text" />
                </div>
                <button type="button" class="search-btn">
                  검색
                  <svg
                    stroke="currentColor"
                    fill="currentColor"
                    stroke-width="0"
                    viewBox="0 0 512 512"
                    height="200px"
                    width="200px"
                    xmlns="http://www.w3.org/2000/svg"
                  >
                    <path
                      d="M456.69 421.39 362.6 327.3a173.81 173.81 0 0 0 34.84-104.58C397.44 126.38 319.06 48 222.72 48S48 126.38 48 222.72s78.38 174.72 174.72 174.72A173.81 173.81 0 0 0 327.3 362.6l94.09 94.09a25 25 0 0 0 35.3-35.3zM97.92 222.72a124.8 124.8 0 1 1 124.8 124.8 124.95 124.95 0 0 1-124.8-124.8z"
                    ></path>
                  </svg>
                </button>
              </div>
            </fieldset>
          </form>
          <!-- <button type="button" class="search-btn pop-btn" data-pop="search">
          검색하기
        </button> -->
        </div>
        <div class="alert-wrap">
          <button type="button" class="alert-btn">알림</button>
        </div>
      </div>

      <!--================ menu ================-->
      <Menu />
    </div>
  </div>
</template>

<script setup>
import Menu from "./Menu.vue";
</script>

<style scope lang="scss">
@import url("/public/css/header.scss");
</style>
