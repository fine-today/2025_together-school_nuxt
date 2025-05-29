<template>
  <nav class="menu" id="menu">
    <div class="depth depth1">
      <ul class="depth-list depth1-list">
        <li
          v-for="(depth1, index) in MENUS"
          :key="index"
          class="depth-item depth1-item"
        >
          <a href="#n" class="depth-anchor depth1-anchor">
            <span>{{ depth1.title }}</span>
          </a>
        </li>
        <!--<li class="depth-item depth1-item">
          <a href="#n" class="depth-anchor depth1-anchor">
            <span>정책제안</span>
          </a>
          <div class="depth depth2">
            <ul class="depth-list depth2-list">
              <li class="depth-item depth2-item">
                <a href="#n" class="depth-anchor depth2-anchor">
                  <span>정책제안</span>
                </a>
              </li>
              <li class="depth-item depth2-item">
                <a href="#n" class="depth-anchor depth2-anchor">
                  <span>정책토론</span>
                </a>
              </li>
              <li class="depth-item depth2-item">
                <a href="#n" class="depth-anchor depth2-anchor">
                  <span>정책답변</span>
                </a>
              </li>
              <li class="depth-item depth2-item">
                <a href="#n" class="depth-anchor depth2-anchor">
                  <span>정책실현</span>
                </a>
              </li>
              <li class="depth-item depth2-item">
                <a href="#n" class="depth-anchor depth2-anchor">
                  <span>함께차담회</span>
                </a>
              </li>
            </ul>
          </div>
        </li>
        <li class="depth-item depth1-item">
          <a href="#n" class="depth-anchor depth1-anchor">
            <span>교원연구실</span>
          </a>
        </li>
        <li class="depth-item depth1-item">
          <a href="#n" class="depth-anchor depth1-anchor">
            <span>함께톡톡</span>
          </a>
        </li>
        <li class="depth-item depth1-item">
          <a href="#n" class="depth-anchor depth1-anchor">
            <span>함께행복</span>
          </a>
        </li>
        <li class="depth-item depth1-item">
          <a href="#n" class="depth-anchor depth1-anchor">
            <span>스터디카페</span>
          </a>
        </li>
        <li class="depth-item depth1-item">
          <a href="#n" class="depth-anchor depth1-anchor">
            <span>공지사항</span>
          </a>
        </li>-->
      </ul>
    </div>
  </nav>
</template>

<script setup>
import { ref } from "vue";
const MENUS = ref([
  {
    id: "0",
    title: "정책제안",
    anchor: "#n",
    active: false,
    sub: [
      {
        id: "0-1",
        title: "We are Misto",
        anchor: "#n",
        active: false,
      },
      {
        id: "0-2",
        title: "연혁",
        anchor: "#n",
        active: false,
      },
      {
        id: "0-3",
        title: "브랜드",
        anchor: "#n",
        active: false,
      },
    ],
  },
  {
    id: "1",
    title: "함께톡톡",
    anchor: "#n",
    active: false,
    sub: [
      {
        id: "0-1",
        title: "재무정보",
        anchor: "#n",
        active: false,
      },
      {
        id: "0-2",
        title: "공시정보",
        anchor: "#n",
        active: false,
      },
      {
        id: "0-3",
        title: "주주총회",
        anchor: "#n",
        active: false,
      },
      {
        id: "0-3",
        title: "주주환원",
        anchor: "#n",
        active: false,
      },
      {
        id: "0-3",
        title: "IR자료",
        anchor: "#n",
        active: false,
      },
      {
        id: "0-3",
        title: "기업지배구조",
        anchor: "#n",
        active: false,
      },
    ],
  },
  {
    id: "2",
    title: "공지사항",
    anchor: "#n",
    active: false,
    sub: [
      {
        id: "0-1",
        title: "ESG 하이라이트",
        anchor: "#n",
        active: false,
      },
      {
        id: "0-2",
        title: "ESG 평가 & 이미셔티브",
        anchor: "#n",
        active: false,
      },
      {
        id: "0-3",
        title: "지속가능경영보고서",
        anchor: "#n",
        active: false,
      },
      {
        id: "0-3",
        title: "ESG 정책",
        anchor: "#n",
        active: false,
      },
    ],
  },
  {
    id: "3",
    title: "마이페이지",
    anchor: "#n",
    active: false,
    sub: [
      {
        id: "0-1",
        title: "문화",
        anchor: "#n",
        active: false,
      },
      {
        id: "0-2",
        title: "복지",
        anchor: "#n",
        active: false,
      },
      {
        id: "0-3",
        title: "채용공고",
        anchor: "#n",
        active: false,
      },
    ],
  },
]);
</script>

<style></style>
