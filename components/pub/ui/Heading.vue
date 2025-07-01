<template>
  <h2 v-if="props.type === 'h2'" :class="props.class"><slot></slot></h2>
  <h3 v-if="props.type === 'h3'" :class="props.class"><slot></slot></h3>
  <h4 v-if="props.type === 'h4'" :class="props.class"><slot></slot></h4>
  <h5 v-if="props.type === 'h5'" :class="props.class"><slot></slot></h5>
  <h6 v-if="props.type === 'h6'" :class="props.class"><slot></slot></h6>
</template>

<script setup>
import { defineProps } from "vue";
const props = defineProps({ type: String, class: String });
</script>

<style scope lang="scss">
h1,
h2,
h3,
h4,
h5,
h6,
.h1,
.h2,
.h3,
.h4,
.h5,
.h6 {
  font-weight: 600;
}
h2,
.h2 {
  font-size: 48px;
}
h3,
.h3 {
  font-size: 36px;
}
h4,
.h4 {
  font-size: 24px;
}
h5,
.h5 {
  font-size: 20px;
}
h6,
.h6 {
  font-size: 18px;
}
</style>
