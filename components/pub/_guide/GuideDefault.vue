<template>
  <div>
    <VCodeBlock
      :code="code"
      highlightjs
      label="Hello World"
      lang="javascript"
      theme="neon-bunny"
    />

    <h1 id="-">퍼블리싱 가이드</h1>
    <h2 id="-">기본사항</h2>
    <h3 id="-">해상도</h3>
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
    <h3 id="-">네이밍 규칙</h3>
    <ul>
      <li>
        <p>
          underline 방식(예 : class_name)이나, 카멜방식(예 : className)은 사용을
          지양한다.
        </p>
      </li>
      <li>
        <p>class name은 스네이크 방식(예 : class-name)으로 한다.</p>
        <pre><code class="lang-html"><span class="hljs-tag">&lt;<span class="hljs-name">div</span> <span class="hljs-attr">class</span>=<span class="hljs-string">"con-list img-list"</span>&gt;</span>
  <span class="hljs-tag">&lt;<span class="hljs-name">div</span> <span class="hljs-attr">class</span>=<span class="hljs-string">"con-item img-item"</span>&gt;</span><span class="hljs-tag">&lt;/<span class="hljs-name">div</span>&gt;</span>

  <span class="hljs-comment">&lt;!-- 잘못된 예 --&gt;</span>
  <span class="hljs-tag">&lt;<span class="hljs-name">div</span> <span class="hljs-attr">class</span>=<span class="hljs-string">"con_list imgList"</span>&gt;</span>
    <span class="hljs-tag">&lt;<span class="hljs-name">div</span> <span class="hljs-attr">class</span>=<span class="hljs-string">"conItem img_item"</span>&gt;</span><span class="hljs-tag">&lt;/<span class="hljs-name">div</span>&gt;</span>
  <span class="hljs-tag">&lt;/<span class="hljs-name">div</span>&gt;</span>
<span class="hljs-tag">&lt;/<span class="hljs-name">div</span>&gt;</span>
</code></pre>
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
    <pre><code class="lang-html"><span class="hljs-tag">&lt;<span class="hljs-name">meta</span> <span class="hljs-attr">http-equiv</span>=<span class="hljs-string">"X-UA-Compatible"</span> <span class="hljs-attr">content</span>=<span class="hljs-string">"IE=edge"</span> /&gt;</span>
<span class="hljs-tag">&lt;<span class="hljs-name">meta</span> <span class="hljs-attr">http-equiv</span>=<span class="hljs-string">"Content-Type"</span> <span class="hljs-attr">content</span>=<span class="hljs-string">"text/html; CHARSET=utf-8"</span> /&gt;</span>
<span class="hljs-tag">&lt;<span class="hljs-name">meta</span> <span class="hljs-attr">http-equiv</span>=<span class="hljs-string">"imagetoolbar"</span> <span class="hljs-attr">content</span>=<span class="hljs-string">"no"</span> /&gt;</span>
<span class="hljs-tag">&lt;<span class="hljs-name">meta</span> <span class="hljs-attr">name</span>=<span class="hljs-string">"Author"</span> <span class="hljs-attr">content</span>=<span class="hljs-string">"www.adcapsule.co.kr"</span> /&gt;</span>
<span class="hljs-tag">&lt;<span class="hljs-name">meta</span> <span class="hljs-attr">name</span>=<span class="hljs-string">"title"</span> <span class="hljs-attr">content</span>=<span class="hljs-string">"title"</span> /&gt;</span>
<span class="hljs-tag">&lt;<span class="hljs-name">meta</span> <span class="hljs-attr">name</span>=<span class="hljs-string">"keywords"</span> <span class="hljs-attr">content</span>=<span class="hljs-string">"홈페이지, EBS, 함께학교"</span> /&gt;</span>
<span class="hljs-tag">&lt;<span class="hljs-name">meta</span> <span class="hljs-attr">name</span>=<span class="hljs-string">"description"</span> <span class="hljs-attr">content</span>=<span class="hljs-string">"함께학교 메인페이지"</span> /&gt;</span>
<span class="hljs-tag">&lt;<span class="hljs-name">meta</span>
  <span class="hljs-attr">name</span>=<span class="hljs-string">"viewport"</span>
  <span class="hljs-attr">content</span>=<span class="hljs-string">"user-scalable=yes, maximum-scale=1.0, width=1004"</span>
/&gt;</span>
/* 모바일일 경우 */

<span class="hljs-comment">&lt;!-- sns 바로가기 썸네일 적용 --&gt;</span>
<span class="hljs-tag">&lt;<span class="hljs-name">meta</span> <span class="hljs-attr">property</span>=<span class="hljs-string">"og:type"</span> <span class="hljs-attr">content</span>=<span class="hljs-string">"website"</span> /&gt;</span>
<span class="hljs-tag">&lt;<span class="hljs-name">meta</span> <span class="hljs-attr">property</span>=<span class="hljs-string">"og:title"</span> <span class="hljs-attr">content</span>=<span class="hljs-string">"페이지 제목"</span> /&gt;</span>
<span class="hljs-tag">&lt;<span class="hljs-name">meta</span> <span class="hljs-attr">property</span>=<span class="hljs-string">"og:description"</span> <span class="hljs-attr">content</span>=<span class="hljs-string">"페이지 설명"</span> /&gt;</span>
<span class="hljs-tag">&lt;<span class="hljs-name">meta</span> <span class="hljs-attr">property</span>=<span class="hljs-string">"og:image"</span> <span class="hljs-attr">content</span>=<span class="hljs-string">"페이지 썸네일 이미지 주소"</span> /&gt;</span>
<span class="hljs-tag">&lt;<span class="hljs-name">meta</span> <span class="hljs-attr">property</span>=<span class="hljs-string">"og:url"</span> <span class="hljs-attr">content</span>=<span class="hljs-string">"페이지 주소"</span> /&gt;</span>

<span class="hljs-comment">&lt;!-- twitter 썸네일 적용 --&gt;</span>
<span class="hljs-tag">&lt;<span class="hljs-name">meta</span> <span class="hljs-attr">property</span>=<span class="hljs-string">"twitter:card"</span> <span class="hljs-attr">content</span>=<span class="hljs-string">"summary"</span> /&gt;</span>
<span class="hljs-tag">&lt;<span class="hljs-name">meta</span> <span class="hljs-attr">property</span>=<span class="hljs-string">"twitter:title"</span> <span class="hljs-attr">content</span>=<span class="hljs-string">"페이지 제목"</span> /&gt;</span>
<span class="hljs-tag">&lt;<span class="hljs-name">meta</span> <span class="hljs-attr">property</span>=<span class="hljs-string">"twitter:description"</span> <span class="hljs-attr">content</span>=<span class="hljs-string">"페이지 설명"</span> /&gt;</span>
<span class="hljs-tag">&lt;<span class="hljs-name">meta</span> <span class="hljs-attr">property</span>=<span class="hljs-string">"twitter:image"</span> <span class="hljs-attr">content</span>=<span class="hljs-string">"페이지 썸네일 이미지 주소"</span> /&gt;</span>
</code></pre>
    <h3 id="-">들여쓰기 규칙</h3>
    <ul>
      <li>마크업이 중첩될 때마다 1탭씩 들여쓰기 한다.</li>
      <li>들어쓰기 공백 기준은 2space로 한다.</li>
    </ul>
    <h3 id="-">폴더구조</h3>
  </div>
</template>

<script setup></script>

<style>
pre {
  border: 1px solid #ddd;
  padding: 20px;
  background-color: #333;
  color: #fff;
}
</style>
