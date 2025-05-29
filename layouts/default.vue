<script setup>
import Header from "@/components/pub/layout/Header.vue";
import Footer from "@/components/pub/layout/Footer.vue";
import Accessibility from "@/components/pub/layout/Accessibility.vue";
</script>

<template>
  <div>
    <Accessibility />
    <Header />
    <slot />
    <Footer />
  </div>
</template>

<style scoped>
.header {
  text-align: center;
  padding: 20px;
}

.header img {
  max-width: 150px;
  height: auto;
}
</style>
