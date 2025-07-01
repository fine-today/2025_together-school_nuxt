<template>
  <div>
    <article class="search-box" v-if="type === 'search'">
      <slot />
    </article>

    <article class="unit-box" v-if="type === 'unit'">
      <div class="left">
        <slot name="left" />
      </div>
      <div class="right">
        <slot name="right" />
      </div>
    </article>

    <article class="board-box" v-if="type === 'board-list'">
      <slot />
    </article>
  </div>
</template>

<script setup>
import { defineProps } from "vue";
defineProps({
  type: String,
});
</script>

<style></style>
