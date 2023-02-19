<template>
    <div v-editable="blok">
      <img
        :src="blok.image.filename + '/m/1600x0'"
        :alt="blok.image.alt"
        class="mx-auto w-3/4 object-cover"
      />
      <div class="container mx-auto mb-12">
        <h1 class="text-6xl text-gray-800 font-bold mt-12 mb-4">{{ blok.title }}</h1>
        <h2 class="text-2xl text-gray-500 font-bold mb-4">
          {{ blok.description }}
        </h2>
        <div class="text-gray-600 mb-3">Written by: <b>{{ blok.author }}</b></div>
        <div v-html="resolvedRichText"></div>
      </div>
    </div>
  </template>
   
  <script setup>
  const props = defineProps({ blok: Object })
   
  const resolvedRichText = computed(() => renderRichText(props.blok.content))
  </script>