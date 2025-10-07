<script setup lang="ts">
import { useRoute } from 'vue-router';

const route = useRoute();
const id = route.params.id as string;

const markdownContent = `
# Hello World

This is **bold** and this is *italic*.

- Item 1
- Item 2
- Item 3
`;

const { data: parsedContent } = await useAsyncData(`article-${id}`, async () => {
  return await parseMarkdown(markdownContent);
});
</script>

<template>
  <ContentLayout>
    <h1 class="text-5xl font-bold">Article {{ id }}</h1>
    <ContentRenderer v-if="parsedContent" class="prose prose-lg max-w-none" :value="parsedContent" />
  </ContentLayout>
</template>