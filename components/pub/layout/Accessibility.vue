<template>
  <div class="accessibility">
    <a href="#menu">주메뉴 바로가기</a>
    <a href="#content">본문 바로가기</a>
  </div>
</template>

<script setup></script>

<style scope lang="scss">
.accessibility {
  position: absolute;
  top: 0;
  left: 0;
  overflow: hidden;
  z-index: 5000;
  width: 100%;
  > a {
    display: block;
    overflow: hidden;
    z-index: 3000;
    height: 1px;
    width: 1px;
    margin: 0 -1px -1px 0;
    font-size: 0;
    line-height: 0;
    text-align: center;
    &:focus,
    &:hover,
    &:active {
      width: auto;
      height: 50px;
      margin: 0;
      padding: 8px 0;
      background: #20262c;
      font-size: 24px;
      font-weight: 700;
      line-height: calc(50px - 16px);
      color: #fff;
    }
  }
}
</style>
