<template>
  <div class="wrap mt-8 mb-8">
    <GuideTop />
    <UTabs :items="items" class="w-full" variant="link" defaultValue="button">
      <template #tabDefault><GuideDefault /> </template>
      <template #text="{ item }">{{ item }}laskfjlsadkfj </template>
      <template #button="{ item }">{{ item }}dlsjkyahflskajf </template>
      <template #form="{ item }">{{ item }}laskfjlsadkfj </template>
      <template #table="{ item }">{{ item }}laskfjlsadkfj </template>
      <template #dialog="{ item }">{{ item }}laskfjlsadkfj </template>
      <template #icons><GuideIcons /> </template>
    </UTabs>
  </div>
</template>

<script setup>
import GuideTop from "~/components/pub/_guide/GuideTop.vue";
import GuideDefault from "~/components/pub/_guide/GuideDefault.vue";
import GuideIcons from "~/components/pub/_guide/GuideIcons.vue";

const items = [
  {
    label: "Default",
    slot: "tabDefault",
  },
  {
    label: "Text",
    slot: "text",
  },
  {
    label: "Button",
    slot: "button",
  },
  {
    label: "Form",
    slot: "form",
  },
  {
    label: "Table",
    slot: "table",
  },
  {
    label: "Dialog",
    slot: "dialog",
  },
  {
    label: "Icons",
    slot: "icons",
  },
];
</script>

<style></style>
