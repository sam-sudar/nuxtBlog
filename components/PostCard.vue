<template>
  <div>
    <h3>{{ post.title }}</h3>
    <p>{{ post.body }}</p>
    <NuxtLink :to="`/posts/${post.id}`">Read More</NuxtLink>
  </div>
</template>

<script setup>
defineProps(["post"]);
</script>
