<template>
  <div
    class="bg-gradient-to-r from-teal-500 to-green-400 p-4 rounded-lg shadow-md"
  >
    <img
      :src="post.image"
      alt="Post Image"
      class="w-full h-40 object-cover rounded-lg mb-4"
    />
    <h3 class="text-xl font-bold text-white">{{ post.title }}</h3>
    <p class="text-sm text-gray-200 truncate">{{ post.description }}</p>
    <NuxtLink
      :to="`/posts/${post.id}`"
      class="text-blue-200 hover:underline mt-2 block"
    >
      Read More
    </NuxtLink>
  </div>
</template>

<script setup>
defineProps(["post"]);
</script>
