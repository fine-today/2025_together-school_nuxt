<template>
  <div>
    <Gnb />

    <!--================ menu-box ================-->
    <div class="menu-box">
      <Menu />
    </div>
  </div>
</template>

<script setup>
import Gnb from "./Gnb.vue";
import Menu from "./Menu.vue";
</script>

<style scope lang="scss">
@import url("/public/css/header.scss");
</style>
