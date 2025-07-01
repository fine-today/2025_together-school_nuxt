<template>
  <div>
    <Heading type="h3" class="mb-5">Input</Heading>
    <UInput v-model="inputValue" />

    <Heading type="h3" class="mb-5 mt-5">Select</Heading>
    <USelect v-model="selectValue" :items="selectItems" class="w-48" />

    <Heading type="h3" class="mb-5 mt-5">checkbox</Heading>
    <div class="flex gap-x-4">
      <UCheckbox label="Check me" required v-model="checkValue" />
      <UCheckbox label="Check me" />
    </div>

    <Heading type="h3" class="mb-5 mt-5">Radio</Heading>
    <URadioGroup v-model="radioValue" :items="radioItems" />

    <Heading type="h3" class="mb-5 mt-5">Calendar</Heading>
    <UCalendar v-model="calendarValue">
      <template #day="{ day }">
        <UChip
          :show="!!getColorByDate(day.toDate('UTC'))"
          :color="getColorByDate(day.toDate('UTC'))"
          size="2xs"
        >
          {{ day.day }}
        </UChip>
      </template>
    </UCalendar>
  </div>
</template>

<script setup>
import { ref } from "vue";
import Heading from "../ui/Heading.vue";
import { CalendarDate } from "@internationalized/date";

/* textfield */
const inputValue = ref("23w45");
/* select */
const selectItems = ref(["Backlog", "Todo", "In Progress", "Done"]);
const selectValue = ref("Backlog");

/* check */
const checkValue = ref(true);

/* radio */
const radioItems = ref(["System", "Light", "Dark"]);
const radioValue = ref("System");

/* calendar */
const calendarValue = ref(new CalendarDate(2022, 2, 3));
function getColorByDate(date) {
  const isWeekend = date.getDay() % 6 == 0;
  const isDayMeeting = date.getDay() % 3 == 0;
  if (isWeekend) {
    return undefined;
  }
  if (isDayMeeting) {
    return "error";
  }
  return "success";
}
</script>

<style></style>
