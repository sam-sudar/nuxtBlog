<template>
  <div class="bg-gray-900 min-h-screen p-6 rounded-lg">
    <h1 class="font-bold text-4xl text-white text-center mb-8">
      Welcome to NuxtStore
    </h1>

    <!-- Products Grid -->
    <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-6">
      <div
        v-for="product in products"
        :key="product.id"
        class="bg-gradient-to-r from-blue-800 to-purple-600 p-4 rounded-xl shadow-lg hover:opacity-90"
      >
        <img
          :src="product.image"
          alt="Product image"
          class="w-full h-64 object-cover rounded-xl mb-4"
        />
        <h3 class="text-white text-xl font-semibold">{{ product.title }}</h3>
        <p class="text-gray-200 text-sm truncate">{{ product.description }}</p>
        <button
          class="bg-purple-500 text-white rounded-full py-2 px-4 mt-2 hover:bg-purple-600"
        >
          Add to Cart
        </button>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref, onMounted } from "vue";

const products = ref([]);

const fetchProducts = async () => {
  const response = await fetch("https://fakestoreapi.com/products");
  const data = await response.json();
  products.value = data;
};

onMounted(() => {
  fetchProducts();
});
</script>

<style scoped>
/* Additional styling for dark theme */
</style>
