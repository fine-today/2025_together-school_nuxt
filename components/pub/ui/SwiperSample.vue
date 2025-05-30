<template>
  <div class="swiper-wrap">
    <swiper
      :modules="modules"
      :slides-per-view="1"
      :space-between="50"
      :navigation="{ enabled: true, prevEl: '.prev', nextEl: '.next' }"
      :pagination="{ clickable: true }"
      :spaceBetween="0"
      @swiper="onSwiper"
      :loop="true"
      @slideChange="onSlideChange"
    >
      <swiper-slide>Slide 1</swiper-slide>
      <swiper-slide>Slide 2</swiper-slide>
      <swiper-slide>Slide 3</swiper-slide>
    </swiper>
    <div class="swiper-ctrl">
      <button type="button" class="ctrl-btn prev">prev</button>
      <button type="button" class="ctrl-btn next">next</button>
    </div>
  </div>
</template>

<script setup>
import { Swiper, SwiperSlide } from "swiper/vue";
import { Navigation, Pagination, Scrollbar, A11y } from "swiper/modules";

import "swiper/css";
import "swiper/css/navigation";
import "swiper/css/pagination";
import "swiper/css/scrollbar";

const onSwiper = () => {
  console.log();
};
const onSlideChange = () => {
  console.log();
};
const modules = [Navigation, Pagination, Scrollbar, A11y];
</script>

<style lang="scss">
.swiper-wrap {
  background-color: #ddd;
  position: relative;
  height: 500px;
  width: 700px;
  margin: 50px auto;
  .swiper {
    height: inherit;
  }
}
.swiper-wrapper {
  height: inherit;
  .swiper-slide {
    height: inherit;
    background-color: #ddd;
  }
}
.swiper-pagination {
  position: absolute;
  bottom: 20px;
  left: 0;
  width: 100%;
}
.swiper-ctrl {
  position: absolute;
  top: 50%;
  left: 50%;
  width: 100%;
  height: 0;
  transform: translateX(-50%);
  .ctrl-btn {
    position: absolute;
    width: 100px;
    height: 100px;
    transform: translateY(-50%);
    border: 1px solid #ddd;
    &.prev {
      right: calc(100% + 10px);
    }
    &.next {
      left: calc(100% + 10px);
    }
  }
}
</style>
