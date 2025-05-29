<template>
  <div class="accessibility">
    <a href="#content">본문 바로가기</a>
  </div>
</template>

<script setup></script>

<style scope>
.accessibility {
  position: relative;
  overflow: hidden;
  z-index: 3000;
  width: 100%;
}
.accessibility a {
  display: block;
  overflow: hidden;
  z-index: 3000;
  height: 1px;
  width: 1px;
  margin: 0 -1px -1px 0;
  font-size: 0;
  line-height: 0;
  text-align: center;
}
.accessibility a:focus,
.accessibility a:hover,
.accessibility a:active {
  width: auto;
  height: 30px;
  margin: 0;
  padding: 8px 0;
  background: #20262c;
  font-size: 14px;
  font-weight: 700;
  line-height: 1;
  color: #fff;
}
</style>
