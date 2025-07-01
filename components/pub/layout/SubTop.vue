<template>
  <div class="sub-top">
    <div class="wrap">
      <div class="title">
        <h2>정책소개</h2>
        <p class="sub-title">
          학생, 학부모, 교원이 함께 소통하는 열린 공간입니다.
        </p>
      </div>
      <div class="icon"><SubTopIcons icon="" /></div>
    </div>
  </div>
  <div class="breadcrumb-wrap">
    <div class="wrap">
      <div class="breadcrumb">
        <ol class="breadcrumb-list">
          <li class="breadcrumb-item">
            <a href="" class="breadcrumb-anchor">
              <Icons icon="home" />
              <span>홈</span>
            </a>
          </li>
          <li class="breadcrumb-item">
            <!--<button type="button" class="breadcrumb-anchor">
            <span></span>
          </button>-->
            <UDropdownMenu
              v-model:open="depth1Open"
              :items="depth1Breadcrumb"
              :content="{
                align: 'start',
                side: 'bottom',
                sideOffset: 8,
              }"
              :ui="{}"
            >
              <UButton
                color="neutral"
                variant="outline"
                class="dropdown-btn"
                :class="depth1Open ? 'active' : ''"
              >
                정책
                <Icons icon="breadReduce" v-if="depth1Open" />
                <Icons icon="breadExpand" v-if="!depth1Open" />
              </UButton>
            </UDropdownMenu>
          </li>
          <li class="breadcrumb-item">
            <UDropdownMenu
              v-model:open="depth2Open"
              :items="depth2Breadcrumb"
              :content="{
                align: 'start',
                side: 'bottom',
                sideOffset: 8,
              }"
              :ui="{}"
            >
              <UButton
                color="neutral"
                variant="outline"
                class="dropdown-btn"
                :class="depth1Open ? 'active' : ''"
              >
                정책소개
                <Icons icon="breadReduce" v-if="depth2Open" />
                <Icons icon="breadExpand" v-if="!depth2Open"
              /></UButton>
            </UDropdownMenu>
          </li>
        </ol>
      </div>

      <div class="sns">
        <button
          type="button"
          class="sns-btn"
          data-sns="naver"
          title="네이버 공유하기(새창)"
        >
          <Icons icon="snsNaver" />
        </button>
        <button
          type="button"
          class="sns-btn"
          data-sns="x"
          title="X 공유하기(새창)"
        >
          <Icons icon="snsX" />
        </button>
        <button
          type="button"
          class="sns-btn"
          data-sns="facebook"
          title="페이스북 공유하기(새창)"
        >
          <Icons icon="snsFacebook" />
        </button>
        <button
          type="button"
          class="sns-btn"
          data-sns="kakaotalk"
          title="카카오톡 공유하기(새창)"
        >
          <Icons icon="snsKakaotalk" />
        </button>
        <button
          type="button"
          class="sns-btn"
          data-sns="copy"
          title="URL 복사하기"
        >
          <Icons icon="snsCopy" />
        </button>
        <button
          type="button"
          class="sns-btn"
          data-sns="brailleDown"
          title="점자 다운로드"
        >
          <Icons icon="snsBrailleDown" />
        </button>
        <button
          type="button"
          class="sns-btn"
          data-sns="brailleViewer"
          title="점자 뷰어보기"
        >
          <Icons icon="snsBrailleViewer" />
        </button>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref, onMounted, defineProps } from "vue";
import { useRouter } from "#app";
import SubTopIcons from "../ui/SubTopIcons.vue";
import Icons from "../ui/Icons.vue";

const router = useRouter();
/*
const menus = reactive({
  id: "policy-introduce",
  title: "정책소개",
  subTitle: "학생, 학부모, 교원이 함께 소통하는 열린 공간입니다.",
  icons: "policy",
});
*/

const depth1Open = ref(false);
const depth2Open = ref(false);
const props = defineProps({ menuId: { type: String } });
onMounted(() => {
  console.log(props.menuId);
});

const depth1Breadcrumb = ref([
  {
    label: "정책",
    onSelect() {
      router.push("/");
    },
  },
  {
    label: "자료실",
    onSelect() {
      router.push("/");
    },
  },
  {
    label: "마이페이지",
    onSelect() {
      router.push("/");
    },
  },
]);

const depth2Breadcrumb = ref([
  {
    label: "정책소개",
    onSelect() {
      router.push("/");
    },
  },
  {
    label: "정책제안",
    onSelect() {
      router.push("/");
    },
  },
  {
    label: "정책토론",
    onSelect() {
      router.push("/");
    },
  },
]);
</script>

<style lang="scss"></style>
