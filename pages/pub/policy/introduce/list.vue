<template>
  <div>
    <Board type="search">
      <USelect v-model="conditionValue" :items="conditionItems" class="w-48" />
      <div class="input">
        <UInput v-model="inputValue" />
        <Icons type="voice" />
      </div>
      <UButton>검색</UButton>
    </Board>

    <Board type="unit">
      <template #left> 1234 </template>
      <template #right> fgsg </template>
    </Board>

    <Board type="board-list">
      <ul class="board-list">
        <li class="board-item">
          <div class="board-con">
            <a href="" class="board-anchor">
              <div class="img">
                <img src="" alt="" />
              </div>
              <div class="title">제목이 들어갑니다. 제목이 들어갑니다.</div>
              <div class="author">작성자명이 들어갑니...</div>
            </a>
            <div class="date">2025.06.26</div>
          </div>
          <div class="count-pbox">
            <div class="board-count">
              <span class="count-item viewer">
                <Icons icon="sns-viewer" />
                <span class="count">2345</span>
              </span>
              <span class="count-item like">
                <Icons icon="sns-like" />
                <span class="count">33444</span>
              </span>
              <span class="count-item reply">
                <Icons icon="sns-reply" />
                <span class="count">33443</span>
              </span>
            </div>
            <div class="attatch">
              <Icons type="attatch" />
            </div>
          </div>
        </li>
      </ul>
    </Board>
  </div>
</template>

<script setup>
import Board from "~/components/pub/ui/Board.vue";
import { ref } from "vue";
import Icons from "~/components/pub/ui/Icons.vue";
const conditionItems = ref([
  {
    label: "제목",
    value: "title",
  },
  {
    label: "내용",
    value: "content",
  },
  {
    label: "작성자",
    value: "author",
  },
]);
const conditionValue = ref("title");

const inputValue = ref("");
</script>

<style></style>
