<template>
  <div class="wrapper" id="wrapper">
    <Accessibility />
    <Header />
    <div class="content" id="content">
      <slot />
    </div>
    <Footer />
  </div>
</template>

<script setup>
import Header from "@/components/pub/layout/Header.vue";
import Footer from "@/components/pub/layout/Footer.vue";
import Accessibility from "@/components/pub/layout/Accessibility.vue";
</script>

<style scoped></style>
