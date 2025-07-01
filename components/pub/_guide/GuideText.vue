<template>
  <Heading type="h2">h2 text 입니다.</Heading>
  <CodeBlock :code="samplecode.h2" />
  <Heading type="h3">h3 text 입니다.</Heading>
  <CodeBlock :code="samplecode.h3" />
  <Heading type="h4">h4 text 입니다.</Heading>
  <CodeBlock :code="samplecode.h4" />
  <Heading type="h5">h5 text 입니다.</Heading>
  <CodeBlock :code="samplecode.h5" />
  <Heading type="h6">h6 text 입니다.</Heading>
  <CodeBlock :code="samplecode.h6" />

  <p>paragraphy 기본 입니다.</p>
  <CodeBlock :code="samplecode.p" />
</template>

<script setup>
import Heading from "@/components/pub/ui/Heading.vue";
import CodeBlock from "@/components/pub/_guide/CodeBlock.vue";

/* heading */
const samplecode = {
  h2: `<Heading type="h2">h2 text 입니다.</Heading>`,
  h3: `<Heading type="h3">h3 text 입니다.</Heading>`,
  h4: `<Heading type="h4">h4 text 입니다.</Heading>`,
  h5: `<Heading type="h5">h5 text 입니다.</Heading>`,
  h6: `<Heading type="h6">h6 text 입니다.</Heading>`,
  p: `<p>paragraphy 기본 입니다.</p>`,
};
</script>

<style></style>
