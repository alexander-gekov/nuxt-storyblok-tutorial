<script setup>
const { slug } = useRoute().params
 
const story = await useAsyncStoryblok(
  slug && slug.length > 0 && slug !== '/' ? slug.join('/') : 'home',
  { version: useRoute().query._storyblok ? 'draft': 'published' }
)
</script>
 
<template>
  <StoryblokComponent v-if="story" :blok="story.content" />
</template>