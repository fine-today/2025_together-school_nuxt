<template>
  <br />
  <ULink to="https://ui.nuxt.com/components/button" target="_blank"
    >Nuxt UI Button 컴포넌트 바로가기
    <UIcon name="material-symbols:arrow-circle-right"
  /></ULink>

  <div class="flex gap-x-2 mt-10">
    <UButton color="primary">primary Button</UButton>
    <UButton color="secondary">secondary Button</UButton>
    <UButton color="success">success Button</UButton>
    <UButton color="info">info Button</UButton>
    <UButton color="warning">warning Button</UButton>
    <UButton color="error">error Button</UButton>
    <UButton color="neutral">neutral Button</UButton>
  </div>
</template>

<script setup></script>
<style>
.iconify {
  color: inherit;
  font-size: inherit;
  position: relative;
  top: 2px;
}
</style>
