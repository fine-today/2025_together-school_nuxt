<template>
  <div class="wrap mt-8 mb-8">
    <GuideTop />
    <UTabs :items="items" class="w-full" variant="link" defaultValue="table">
      <template #tabDefault><GuideDefault /> </template>
      <template #text><GuideText /> </template>
      <template #button><GuideBtns /> </template>
      <template #form><GuideForm /> </template>
      <template #table><GuideTable /></template>
      <template #dialog><GuideDialog /></template>
      <template #icons><GuideIcons /> </template>
      <template #etc><GuideEtc /> </template>
    </UTabs>
  </div>
</template>

<script setup>
import GuideTop from "~/components/pub/_guide/GuideTop.vue";
import GuideDefault from "~/components/pub/_guide/GuideDefault.vue";
import GuideText from "~/components/pub/_guide/GuideText.vue";
import GuideBtns from "~/components/pub/_guide/GuideBtns.vue";
import GuideForm from "~/components/pub/_guide/GuideForm.vue";
import GuideTable from "~/components/pub/_guide/GuideTable.vue";
import GuideDialog from "~/components/pub/_guide/GuideDialog.vue";
import GuideIcons from "~/components/pub/_guide/GuideIcons.vue";
import GuideEtc from "~/components/pub/_guide/GuideEtc.vue";

const emit = defineEmits(["menuId"]);
emit("menuId", "policy-introduce");

const items = [
  {
    label: "Default",
    slot: "tabDefault",
    value: "tabDefault",
  },
  {
    label: "Text",
    slot: "text",
    value: "text",
  },
  {
    label: "Button",
    slot: "button",
    value: "button",
  },
  {
    label: "Form",
    slot: "form",
    value: "form",
  },
  {
    label: "Table",
    slot: "table",
    value: "table",
  },
  {
    label: "Dialog",
    slot: "dialog",
    value: "dialog",
  },
  {
    label: "Icons",
    slot: "icons",
    value: "icons",
  },
  {
    label: "Etc",
    slot: "etc",
    value: "etc",
  },
];
</script>

<style></style>
