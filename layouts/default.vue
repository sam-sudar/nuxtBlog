<template>
  <div>
    <header class="bg-gradient-to-r from-blue-800 to-purple-700 p-4 shadow-md">
      <div class="container mx-auto flex justify-between items-center">
        <!-- Logo Section -->
        <div class="text-white text-2xl font-bold">NuxtStore</div>

        <!-- Navbar Links -->
        <nav class="space-x-6">
          <NuxtLink to="/" class="text-white hover:text-gray-300"
            >Home</NuxtLink
          >
          <NuxtLink to="/cart" class="text-white hover:text-gray-300"
            >Cart</NuxtLink
          >
          <NuxtLink to="/wishlist" class="text-white hover:text-gray-300"
            >Wishlist</NuxtLink
          >
        </nav>

        <!-- Cart and Wishlist Buttons -->
      </div>
    </header>
    <main class="container mx-auto py-8 rounded-md">
      <slot />
    </main>
    <footer class="bg-gray-800 text-white text-center py-4">
      &copy; 2024 nuxtBlog. All rights reserved.
    </footer>
  </div>
</template>

<style>
* {
  font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
}
</style>
