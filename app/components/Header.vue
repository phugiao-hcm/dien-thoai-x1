<template>
  <header class="bg-white shadow-md sticky top-0 z-50">
    <div class="max-w-7xl mx-auto px-4 py-4 flex justify-between items-center">
      <!-- Logo -->
      <NuxtLink to="/" class="text-2xl font-bold text-gray-900">
        iStore
      </NuxtLink>

      <!-- Hamburger Icon (Mobile) -->
      <button
        @click="isOpen = !isOpen"
        class="md:hidden text-gray-800 focus:outline-none"
      >
        <svg
          v-if="!isOpen"
          xmlns="http://www.w3.org/2000/svg"
          class="h-6 w-6"
          fill="none"
          viewBox="0 0 24 24"
          stroke="currentColor"
        >
          <path
            stroke-linecap="round"
            stroke-linejoin="round"
            stroke-width="2"
            d="M4 6h16M4 12h16M4 18h16"
          />
        </svg>
        <svg
          v-else
          xmlns="http://www.w3.org/2000/svg"
          class="h-6 w-6"
          fill="none"
          viewBox="0 0 24 24"
          stroke="currentColor"
        >
          <path
            stroke-linecap="round"
            stroke-linejoin="round"
            stroke-width="2"
            d="M6 18L18 6M6 6l12 12"
          />
        </svg>
      </button>

      <!-- Desktop Navigation -->
      <nav class="hidden md:flex space-x-6 text-gray-700">
        <NuxtLink to="/" class="hover:text-blue-600">Trang chủ</NuxtLink>
        <NuxtLink to="/iphone" class="hover:text-blue-600">iPhone</NuxtLink>
        <NuxtLink to="/accessories" class="hover:text-blue-600"
          >Phụ kiện</NuxtLink
        >
        <NuxtLink to="/support" class="hover:text-blue-600">Hỗ trợ</NuxtLink>
      </nav>
    </div>

    <!-- Mobile Navigation -->
    <div v-if="isOpen" class="md:hidden px-4 pb-4 space-y-2 text-gray-700">
      <NuxtLink to="/" class="block hover:text-blue-600">Trang chủ</NuxtLink>
      <NuxtLink to="/iphone" class="block hover:text-blue-600">iPhone</NuxtLink>
      <NuxtLink to="/accessories" class="block hover:text-blue-600"
        >Phụ kiện</NuxtLink
      >
      <NuxtLink to="/support" class="block hover:text-blue-600"
        >Hỗ trợ</NuxtLink
      >
    </div>
  </header>
</template>

<script setup>
import { ref } from "vue";
const isOpen = ref(false);
</script>
