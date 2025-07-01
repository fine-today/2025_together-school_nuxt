<template>
  <div>
    <Heading type="h3">Table(Nuxt UI 사용하지 않음.)</Heading>
    <div class="table-wrap">
      <table class="table">
        <caption>
          테이블 제목 - 테이블th 나열
        </caption>
        <colgroup>
          <col />
          <col :style="{ width: widthSize + 'px' }" />
          <col style="width: 120px" />
          <col style="width: 120px" />
        </colgroup>
        <thead>
          <tr>
            <th scope="col">th입니다.</th>
            <th scope="col" class="text-left">
              left 정렬입니다. tailwind 적용
            </th>
            <th scope="col">th입니다.</th>
            <th scope="col">th입니다.</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th scope="row">dksajlfk</th>
            <td>td입니다.</td>
            <td>td입니다.</td>
            <td>td입니다.</td>
          </tr>
          <tr>
            <th scope="row">2.dksajlfk</th>
            <td>td입니다.</td>
            <td>td입니다.</td>
            <td>td입니다.</td>
          </tr>
        </tbody>
      </table>
    </div>
  </div>
</template>

<script setup>
import Heading from "../ui/Heading.vue";
import { ref } from "vue";

const widthSize = ref(20);
</script>

<style lang="scss">
.table-wrap {
  position: relative;
  .table {
    width: 100%;
    border-top: 1px solid #ddd;
    border-left: 1px solid #ddd;
    caption,
    colgroup {
      position: absolute;
      left: 0;
      top: 0;
      opacity: 0;
    }
    th,
    td {
      border-right: 1px solid #ddd;
      border-bottom: 1px solid #ddd;
      padding: 8px 12px;
    }
    thead {
      th {
        background-color: #e7f0f3;
        font-weight: 600;
      }
    }
    tbody {
      th {
        background-color: #f3f6f7;
      }
    }
  }
}
</style>
