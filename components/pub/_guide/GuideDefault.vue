<template>
  <div>
    <h1>퍼블리싱 가이드</h1>
    <h2>기본사항</h2>
    <h3>해상도</h3>
    <ul>
      <li>기본 해상도 : 1902*1024</li>
      <li>
        Break Point
        <ul>
          <li>tablet : 769 ~ 1280</li>
          <li>mobile : 360 ~768</li>
        </ul>
      </li>
    </ul>
    <h3>네이밍 규칙</h3>
    <ul>
      <li>
        <p>
          underline 방식(예 : class_name)이나, 카멜방식(예 : className)은 사용을
          지양한다.
        </p>
      </li>
      <li>
        <p>class name은 스네이크 방식(예 : class-name)으로 한다.</p>
      </li>
      <li>
        <p>네이밍 시, 약어 사용을 지양한다.</p>
        <ul>
          <li>예약어 : btn : 버튼, img, con, ctrl 등</li>
          <li>잘못된 예 : desc, acc, exmp 등</li>
        </ul>
      </li>
    </ul>
    <h3 id="meta-tag-sns-">META TAG (SNS 썸네일 적용 부분 테스트 필요)</h3>
    <CodeBlock :code="sampleCode.meta" language="html" />

    <h3 id="-">들여쓰기 규칙</h3>
    <ul>
      <li>마크업이 중첩될 때마다 1탭씩 들여쓰기 한다.</li>
      <li>들어쓰기 공백 기준은 2space로 한다.</li>
    </ul>
    <h3 id="-">폴더구조</h3>
  </div>
</template>

<script setup>
import CodeBlock from "@/components/pub/_guide/CodeBlock.vue";
const sampleCode = {
  meta: `<meta http-equiv="X-UA-Compatible" content="IE=edge" />
<meta http-equiv="Content-Type" content="text/html; CHARSET=utf-8" />
<meta http-equiv="imagetoolbar" content="no" />
<meta name="Author" content="www.adcapsule.co.kr" />
<meta name="title" content="title" />
<meta name="keywords" content="홈페이지, EBS, 함께학교" />
<meta name="description" content="함께학교 메인페이지" />
<meta
  name="viewport"
  content="user-scalable=yes, maximum-scale=1.0, width=1004"
/>
/* 모바일일 경우 */

<!-- sns 바로가기 썸네일 적용 -->
<meta property="og:type" content="website" />
<meta property="og:title" content="페이지 제목" />
<meta property="og:description" content="페이지 설명" />
<meta property="og:image" content="페이지 썸네일 이미지 주소" />
<meta property="og:url" content="페이지 주소" />

<!-- twitter 썸네일 적용 -->
<meta property="twitter:card" content="summary" />
<meta property="twitter:title" content="페이지 제목" />
<meta property="twitter:description" content="페이지 설명" />
<meta property="twitter:image" content="페이지 썸네일 이미지 주소" />`,
};
</script>

<style>
/*pre {
  border: 1px solid #ddd;
  padding: 20px;
  background-color: #333;
  color: #fff;
}*/
</style>
