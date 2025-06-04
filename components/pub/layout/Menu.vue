<template>
  <nav class="menu" id="menu">
    <div class="wrap">
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
            <div class="depth depth2" v-if="depth1.sub !== undefined">
              <ul class="depth-list depth2-list">
                <li
                  class="depth-item depth2-item"
                  v-for="(depth2, depth2Index) in depth1.sub"
                  :key="depth2Index"
                >
                  <a href="#n" class="depth-anchor depth2-anchor">
                    <span>{{ depth2.title }}</span>
                  </a>
                </li>
              </ul>
              <span class="depth2-bg">
                <Icons :icon="depth1.icons" />
              </span>
            </div>
          </li>
        </ul>
      </div>
    </div>
  </nav>
</template>

<script setup>
import { ref } from "vue";
import Icons from "@/components/pub/ui/Icons.vue";
const MENUS = ref([
  {
    id: "0",
    title: "정책",
    anchor: "#n",
    active: false,
    icons: `policy`,
    sub: [
      {
        id: "0-1",
        title: "정책소개",
        anchor: "#n",
        active: false,
      },
      {
        id: "0-2",
        title: "정책제안",
        anchor: "#n",
        active: false,
      },
      {
        id: "0-3",
        title: "정책토론",
        anchor: "#n",
        active: false,
      },
      {
        id: "0-3",
        title: "정책답변",
        anchor: "#n",
        active: false,
      },
      {
        id: "0-3",
        title: "정책실현",
        anchor: "#n",
        active: false,
      },
    ],
  },
  {
    id: "1",
    title: "자료실",
    anchor: "#n",
    active: false,
    icons: `storage`,
    sub: [
      {
        id: "1-1",
        title: "영상나눔",
        anchor: "#n",
        active: false,
      },
      {
        id: "1-2",
        title: "교육 TV",
        anchor: "#n",
        active: false,
      },
      {
        id: "1-3",
        title: "이벤트",
        anchor: "#n",
        active: false,
      },
      {
        id: "1-4",
        title: "공지사항",
        anchor: "#n",
        active: false,
      },
      {
        id: "1-5",
        title: "보도자료",
        anchor: "#n",
        active: false,
      },
    ],
  },
  {
    id: "2",
    title: "마이페이지",
    anchor: "#n",
    active: false,
    icons: `mypage`,
    sub: [
      {
        id: "2-1",
        title: "임시저장글",
        anchor: "#n",
        active: false,
      },
      {
        id: "2-2",
        title: "내 글",
        anchor: "#n",
        active: false,
      },
      {
        id: "2-3",
        title: "내 댓글",
        anchor: "#n",
        active: false,
      },
      {
        id: "2-4",
        title: "알림",
        anchor: "#n",
        active: false,
      },
      {
        id: "2-5",
        title: "알림설정",
        anchor: "#n",
        active: false,
      },
      {
        id: "2-6",
        title: "회원정보",
        anchor: "#n",
        active: false,
      },
    ],
  },
]);
</script>

<style></style>
