<template>
  <!-- Accordion -->
  <Heading type="h3">Accordion</Heading>
  <Heading type="h4">간단 버전</Heading>
  <UAccordion :items="accordionList" />

  <Heading type="h4">inner-content 버전</Heading>

  <UAccordion :items="accordionList">
    <template #content="{ item }">
      <p class="pb-3.5 text-sm text-muted" v-if="item.label === 'Icons'">
        This is the icon panel.
      </p>
      <p class="pb-3.5 text-sm text-muted">
        This is the {{ item.label }} panel.
      </p>
    </template>
  </UAccordion>

  <!-- Modal -->
  <Heading type="h3" class="mt-4 mb-3">Modal</Heading>
  <UModal title="타이틀을 입력">
    <UButton label="일반 Modal" color="neutral" variant="subtle" class="mb-2" />

    <template #body>
      <Placeholder class="h-48" />
      콘텐츠를 입력해주세요.
    </template> </UModal
  ><br />

  <UModal :overlay="false" title="타이틀 입력" v-model:open="open">
    <UButton label="mount시 oepn" color="neutral" variant="subtle" />

    <template #body>
      <Placeholder class="h-48" />
    </template>
  </UModal>
  <!-- pop over -->
  <Heading type="h3" class="mt-4 mb-3">Pop-over</Heading>

  <UPopover :content="{ sideOffset: 10, align: 'start' }">
    <UButton label="기간선택" color="neutral" variant="subtle" />

    <template #content>
      <div class="period flex">
        <h4>기간</h4>
        <div class="period-list">
          <button type="button" class="period-btn">전체</button>
          <button type="button" class="period-btn">1주일</button>
          <button type="button" class="period-btn">1개월</button>
          <button type="button" class="period-btn">3개월</button>
          <button type="button" class="period-btn">6개월</button>
          <button type="button" class="period-btn">직접입력</button>
        </div>
      </div>

      <div class="date flex">
        <div class="start">
          <USelect
            v-model="selectValue.start.year"
            :items="selectItems.start.year"
            class="w-48"
          />
          <span class="unit">년</span>
          <USelect
            v-model="selectValue.start.month"
            :items="selectItems.start.month"
            class="w-48"
          />
          <span class="unit">월</span>
          <USelect
            v-model="selectValue.start.date"
            :items="selectItems.start.date"
            class="w-48"
          />
          <span class="unit">일</span>
        </div>
        <div class="split">~</div>
        <div class="start">
          <USelect
            v-model="selectValue.end.year"
            :items="selectItems.end.year"
            class="w-48"
          />
          <span class="unit">년</span>
          <USelect
            v-model="selectValue.end.month"
            :items="selectItems.end.month"
            class="w-48"
          />
          <span class="unit">월</span>
          <USelect
            v-model="selectValue.end.date"
            :items="selectItems.end.date"
            class="w-48"
          />
          <span class="unit">일</span>
        </div>
      </div>

      <Placeholder class="w-full aspect-square" />
    </template>
  </UPopover>

  <!-- toast -->
  <Heading type="h3" class="mt-4 mb-3">toast</Heading>

  <UPopover :content="{ sideOffset: 10, align: 'start' }">
    <UButton label="toast" color="neutral" variant="subtle" />
    <template #content>
      <Placeholder
        class="w-full aspect-square"
        style="height: 100px; width: 100%; background-color: #ddd"
    /></template>
  </UPopover>
</template>

<script setup>
import { ref, reactive } from "vue";
import Heading from "../ui/Heading.vue";
const open = ref(false);
const accordionList = ref([
  {
    label: "Icons",
    icon: "i-lucide-smile",
    content: "You have nothing to do, @nuxt/icon will handle it automatically.",
  },
  {
    label: "Colors",
    icon: "i-lucide-swatch-book",
    content:
      "Choose a primary and a neutral color from your Tailwind CSS theme.",
  },
  {
    label: "Components",
    icon: "i-lucide-box",
    content:
      "You can customize components by using the `class` / `ui` props or in your app.config.ts.",
  },
]);

/* select1 */
const selectItems = reactive({
  start: {
    year: ["2021", "2022", "2023", "2024", "2025"],
    month: ["1", "2", "3", "4", "5", "6", "7", "8", "9", "10", "11", "12"],
    date: [
      "1",
      "2",
      "3",
      "4",
      "5",
      "6",
      "7",
      "8",
      "9",
      "10",
      "11",
      "12",
      "13",
      "14",
      "15",
      "16",
      "17",
      "18",
      "19",
    ],
  },

  end: {
    year: ["2021", "2022", "2023", "2024", "2025"],
    month: ["1", "2", "3", "4", "5", "6", "7", "8", "9", "10", "11", "12"],
    date: [
      "1",
      "2",
      "3",
      "4",
      "5",
      "6",
      "7",
      "8",
      "9",
      "10",
      "11",
      "12",
      "13",
      "14",
      "15",
      "16",
      "17",
      "18",
      "19",
    ],
  },
});
const selectValue = reactive({
  start: {
    year: "2021",
    month: "2",
    date: "10",
  },
  end: {
    year: "2024",
    month: "4",
    date: "12",
  },
});
</script>

<style></style>
