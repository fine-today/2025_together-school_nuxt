<template>
  <div>
    <NuxtRouteAnnouncer />
    <!-- <NuxtWelcome /> -->
    <SwiperSample />
  </div>
</template>

<script setup>
import SwiperSample from "@/components/pub/ui/SwiperSample.vue";
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
    background-color: #333;
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
