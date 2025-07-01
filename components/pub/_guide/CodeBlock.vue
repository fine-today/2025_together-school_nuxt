<template>
  <div class="code-block">
    <Prism :language="language" class="line-numbers">{{ code }}</Prism>
    <button @click="copyCode(code)" class="copy-btn">
      <svg
        stroke="currentColor"
        fill="currentColor"
        stroke-width="0"
        viewBox="0 0 24 24"
        height="1em"
        width="1em"
        xmlns="http://www.w3.org/2000/svg"
      >
        <path fill="none" d="M0 0h24v24H0V0z"></path>
        <path
          d="M16 1H4c-1.1 0-2 .9-2 2v14h2V3h12V1zm3 4H8c-1.1 0-2 .9-2 2v14c0 1.1.9 2 2 2h11c1.1 0 2-.9 2-2V7c0-1.1-.9-2-2-2zm0 16H8V7h11v14z"
        ></path>
      </svg>
    </button>
  </div>
</template>

<script setup>
//import "prismjs/themes/prism-okaidia.css";
//import "prismjs/plugins/line-numbers/prism-line-numbers.css";
import Prism from "vue-prism-component";
import { defineProps, onMounted } from "vue";
import PrismJS from "prismjs";
const props = defineProps({ code: String, language: String });

function copyCode() {
  navigator.clipboard.writeText(props.code).then(() => {
    alert("복사되었습니다!");
  });
}
onMounted(() => {
  PrismJS.highlightAll();
});
</script>

<style lang="scss" scope>
.code-block {
  position: relative;
  .copy-btn {
    display: flex;
    align-items: center;
    justify-content: center;
    position: absolute;
    right: 8px;
    top: 8px;
    width: 24px;
    height: 28px;
    background-color: #333;
    border: 1px solid #444;
    border-radius: 4px;
    color: #999;
    font-weight: 600;
  }
}
</style>
