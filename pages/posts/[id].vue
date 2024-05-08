<script setup lang="ts">
import type {Post} from "@/interfaces/posts.type.ts";

const { id } = useRoute().params;

const { data: posts } = await useFetch<Post>(
  `https://jsonplaceholder.typicode.com/posts/${id}`
);
</script>

<template>
  <h1>Post Page id: {{ id }}</h1>
  <h2>{{ posts?.title }}</h2>
  <p>
    {{ posts?.body }}
  </p>
</template>
