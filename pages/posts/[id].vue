<template>
  <div>
    <h2>{{ post.title }}</h2>
    <p>{{ post.body }}</p>
    <NuxtLink to="/">Back to Home</NuxtLink>
  </div>
</template>

<script setup>
import { useRoute } from "vue-router";

const route = useRoute();
const post = {
  id: route.params.id,
  title: `Post ${route.params.id}`,
  body: "Full post content here.",
};
</script>
