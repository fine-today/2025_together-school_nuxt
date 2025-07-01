<template>
  <div>
    <h3>layout</h3>
    <ul class="list">
      <li
        class="item"
        :class="iconList.mode === 'dark' ? 'dark' : 'white'"
        v-for="iconList in iconsLists"
        :key="iconList.id"
      >
        <Icons :icon="iconList.id" />
        <span class="title">{{ iconList.title }}</span>
      </li>
    </ul>

    <h3>logos</h3>
    <h4>기본모드</h4>
    <ul class="list">
      <li class="item" v-for="logoList in logoLists" :key="logoList.language">
        <Logos mode="light" :language="logoList.language" />
        <span class="title">
          <span>{{ logoList.title }}</span>
        </span>
      </li>
    </ul>
    <h4>다크모드</h4>
    <ul class="list">
      <li
        class="item dark"
        v-for="logoList in logoLists"
        :key="'dark-' + logoList.language"
      >
        <Logos mode="dark" :language="logoList.language" />
        <span class="title">
          <span>{{ logoList.title }}</span>
        </span>
      </li>
    </ul>
  </div>
</template>

<script setup>
import { reactive } from "vue";
import Icons from "/components/pub/ui/Icons.vue";
import Logos from "/components/pub/ui/Logos.vue";

const logoLists = reactive([
  { language: "ko", title: "한국어" },
  { language: "en", title: "영어" },
  { language: "ja", title: "일본어" },
  { language: "zh-CN", title: "중국어_간체" },
  { language: "zh-TW", title: "중국어_번체" },
  { language: "vi", title: "베트남어" },
  { language: "it", title: "이탈리아어" },
  { language: "th", title: "태국어" },
  { language: "id", title: "인도네시아어" },
  { language: "fr", title: "프랑스어" },
  { language: "es", title: "스페인어" },
  { language: "ru", title: "러시아어" },
  { language: "de", title: "독일어" },
]);
const iconsLists = reactive([
  {
    id: "modeDark",
    title: "modeDark",
  },
  {
    id: "modeBright",
    title: "modeBright",
  },
  {
    id: "reduce",
    title: "reduce",
  },
  {
    id: "expand",
    title: "expand",
  },
  {
    id: "brailleDown",
    title: "brailleDown",
  },
  {
    id: "brailleViewer",
    title: "brailleViewer",
  },
  {
    id: "voice",
    title: "voice",
  },
  {
    id: "search",
    title: "search",
    mode: "dark",
  },
  {
    id: "login",
    title: "login",
  },
  {
    id: "join",
    title: "join",
  },
  {
    id: "language",
    title: "language",
  },
  {
    id: "policy",
    title: "policy",
    mode: "dark",
  },
  {
    id: "storage",
    title: "storage",
    mode: "dark",
  },
  {
    id: "mypage",
    title: "mypage",
    mode: "dark",
  },
  {
    id: "mainIntroduce",
    title: "mainIntroduce",
  },
  {
    id: "mainProposal",
    title: "mainProposal",
  },
  {
    id: "mainDiscussion",
    title: "mainDiscussion",
  },
  {
    id: "mainAnswer",
    title: "mainAnswer",
  },
  {
    id: "mainRealization",
    title: "mainRealization",
  },
  {
    id: "notice",
    title: "notice",
  },
  {
    id: "video",
    title: "video",
  },
  {
    id: "play",
    title: "play",
  },
  {
    id: "home",
    title: "home",
  },
  {
    id: "breadExpand",
    title: "breadExpand",
  },
  {
    id: "breadReduce",
    title: "breadReduce",
  },
  {
    id: "snsNaver",
    title: "snsNaver",
  },
  {
    id: "snsX",
    title: "snsX",
  },
  {
    id: "snsFacebook",
    title: "snsFacebook",
  },
  {
    id: "snsKakaotalk",
    title: "snsKakaotalk",
  },
  {
    id: "snsCopy",
    title: "snsCopy",
  },
  {
    id: "snsBrailleDown",
    title: "snsBrailleDown",
  },
  {
    id: "snsBrailleViewer",
    title: "snsBrailleViewer",
  },
  {
    id: "viewCount",
    title: "viewCount",
  },
  {
    id: "likeCount",
    title: "likeCount",
  },
  {
    id: "commentCount",
    title: "commentCount",
  },
  {
    id: "attatch",
    title: "attatch",
  },
  {
    id: "",
    title: "",
  },
  {
    id: "",
    title: "",
  },
  {
    id: "",
    title: "",
  },
  {
    id: "",
    title: "",
  },
]);
</script>

<style scope lang="scss">
.list {
  display: grid;
  grid-template-columns: repeat(6, 1fr);
  border-top: 1px solid #ddd;
  border-left: 1px solid #ddd;
  .item {
    border-right: 1px solid #ddd;
    border-bottom: 1px solid #ddd;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: space-between;
    text-align: center;

    &.dark {
      background-color: #666;
    }
    .svg-icon,
    .logo-box {
      padding: 20px;
      display: flex;
      align-items: center;
      justify-content: center;
      height: 150px;
      svg {
        max-width: 100%;
        max-height: 100%;
      }
    }
    .title {
      border-top: 1px solid #ddd;
      width: 100%;
      height: 52px;
      padding: 10px;
      display: flex;
      align-content: center;
      justify-content: center;
      background-color: rgb(13, 158, 86);
      color: #fff;
      font-weight: 700;
    }
  }
}
</style>
