<script setup lang="ts">
interface CardMainProps {
  title: string;
  body: string;
  id: number;
}

const { title, body, id } = defineProps<CardMainProps>();
</script>

<template>
  <h2>{{ id }} {{ title }}</h2>
  <p>{{ body }}</p>

  <NuxtLink :to="`/posts/${id}`">Read More</NuxtLink>
</template>
