<template>
  <nav class="menu over" id="menu" ref="menuElem">
    <div class="menu-wrap" :style="{ height: menuHeight + 'px' }">
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
            <div
              class="depth depth2"
              v-if="depth1.sub !== undefined"
              :ref="
                (el) => {
                  if (el) itemsRefs[index] = el;
                }
              "
            >
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
import { onMounted, onBeforeUnmount, reactive, ref } from "vue";
import Icons from "@/components/pub/ui/Icons.vue";
const MENUS = reactive([
  {
    id: "0",
    title: "정책",
    anchor: "#n",
    active: false,
    icons: "policy",
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

/* 높이값 산출 */
const menuElem = ref(null);
const itemsRefs = ref([]);
const menuHeight = ref(70);
const fullHeight = ref(70);
const menuHoverEvent = () => {
  menuElem.value.classList.add("over");
  menuHeight.value = fullHeight.value;
};
const menuBlurEvent = () => {
  menuElem.value.classList.remove("over");
  menuHeight.value = 70;
};
onMounted(() => {
  setTimeout(() => {
    itemsRefs.value.forEach((item) => {
      if (item) {
        if (item.offsetHeight > fullHeight.value) {
          fullHeight.value = item.offsetHeight;
        }
      }
    });
    fullHeight.value = fullHeight.value + 70;
    if (menuElem.value) {
      menuElem.value.addEventListener("mouseover", menuHoverEvent);
      menuElem.value.addEventListener("focusin", menuHoverEvent);
      menuElem.value.addEventListener("mouseleave", menuBlurEvent);
      menuElem.value.addEventListener("focusout", menuBlurEvent);
    }
  }, 0);
});

onBeforeUnmount(() => {
  setTimeout(() => {
    if (menuElem.value) {
      menuElem.value.removeEventListener("mouseover", menuHoverEvent);
      menuElem.value.removeEventListener("focusin", menuHoverEvent);
      menuElem.value.removeEventListener("mouseleave", menuBlurEvent);
      menuElem.value.removeEventListener("focusout", menuBlurEvent);
    }
  }, 0);
});
</script>

<style></style>
