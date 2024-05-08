<script setup lang="ts">
import type Post from "@/interfaces/posts.type";

const { data: posts } = await useFetch<Post[]>(
  "https://jsonplaceholder.typicode.com/posts"
);
</script>

<template>
  <h1>Posts Page</h1>
  <CardMain
    v-for="{ id, body, title } in posts"
    :key="id"
    :title="title"
    :body="body"
    :id="id"
  />
</template>
