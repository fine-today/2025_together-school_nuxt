<template>
  <div class="header-banner">
    <a href="#n">
      <div
        class="img"
        style="
          background-image: url(https://www.togetherschool.go.kr/upload/popupbanner/277e01f0b8e94ac4bd3275da5ba98e3e.png);
        "
      ></div>
    </a>
    <button type="button" class="close">닫기</button>
  </div>
</template>

<script setup></script>

<style lang="scss">
.header-banner {
  grid-area: header-banner;
  height: 90px;
  position: relative;
  > a {
    display: block;
    height: 100%;
    width: 100%;
  }
  .img {
    width: 100%;
    height: 100%;
    background-position: center center;
    background-size: cover;
  }
  .close {
    position: absolute;
    width: 40px;
    height: 40px;
    right: 40px;
    top: 25px;
    font-size: 0;
    line-height: 0;
    border: 0;
    background-color: transparent;
    &::before,
    &::after {
      display: block;
      position: absolute;
      left: calc(50% - 12px);
      top: calc(50% - 1px);
      width: 24px;
      height: 2px;
      background-color: #333;
    }
    &::before {
      transform: rotate(45deg);
      transform-origin: center center;
    }
    &::after {
      transform: rotate(-45deg);
      transform-origin: center center;
    }
  }
}
</style>
