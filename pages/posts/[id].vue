<template>
  <div class="bg-gray-100 min-h-screen p-6">
    <h1 class="text-3xl font-bold text-gray-800 mb-4">{{ post.title }}</h1>
    <p class="text-gray-700">{{ post.body }}</p>
    <NuxtLink to="/" class="text-blue-600 hover:underline mt-4 inline-block">
      Back to Home
    </NuxtLink>
  </div>
</template>

<script setup>
import { useRoute } from "vue-router";

const route = useRoute();
const postId = route.params.id;

const posts = [
  {
    id: 1,
    title: "First Blog Post",
    body: "This is the body of the first post.",
  },
  {
    id: 2,
    title: "Second Blog Post",
    body: "This is the body of the second post.",
  },
  {
    id: 3,
    title: "Third Blog Post",
    body: "This is the body of the third post.",
  },
];

const post = posts.find((p) => p.id === Number(postId));
</script>
