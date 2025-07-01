<template>
  <NuxtLayout :menuId="menuId">
    <NuxtPage @menuId="updateMenuId" />
  </NuxtLayout>
</template>

<script setup>
import { ref } from "vue";
const menuId = ref("");
function updateMenuId(value) {
  menuId.value = value;
}

// meta 요소 추가
useHead({
  bodyAttrs: {
    "data-site": "sub",
  },
  meta: [
    { "http-equiv": "X-UA-Compatible", content: "IE=edge" },
    { "http-equiv": "Content-Type", content: "text/html; CHARSET=utf-8" },
    { "http-equiv": "imagetoolbar", content: "no" },
    { name: "Author", content: "www.togetherschool.go.kr" },
    { name: "title", content: "함께학교 장애인 사이트" },
    //{ name: "", content: "" },
    {
      name: "description",
      content: "함께학교 장애인 사이트",
    },
    {
      name: "keywords",
      content: "홈페이지, EBS, 함께학교",
    },
    {
      name: "viewport",
      content: "user-scalable=yes, maximum-scale=1.0, width=1280",
    },
    {
      property: "og:title",
      content: "My Nuxt Page",
    },
    {
      property: "og:type",
      content: "website",
    },
    {
      property: "og:description",
      content: "홈페이지, EBS, 함께학교",
    },
    {
      property: "og:image",
      content: "페이지 썸네일 이미지 주소",
    },
    {
      property: "og:url",
      content: "페이지 주소",
    },
    {
      property: "twitter:card",
      content: "summary",
    },
    {
      property: "twitter:title",
      content: "페이지 제목",
    },
    {
      property: "twitter:description",
      content: "페이지 설명",
    },
    {
      property: "twitter:image",
      content: "페이지 썸네일 이미지 주소",
    },
  ],
});
/*  페이지별 SEO 화면 설정 필요 */
</script>
