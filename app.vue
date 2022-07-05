<script setup lang="ts">
useHead({
  title: 'Nuxt 3 + Tailwind CSS',
});

const count = ref(0);

const increment = () => count.value++;
const decrement = () => count.value--;
</script>

<template>
  <div
    class="container mx-auto h-screen py-4 text-center grid place-items-center"
  >
    <div>
      <h1 class="text-center text-3xl font-semibold">Nuxt 3 + Tailwind CSS</h1>
      <p class="text-6xl font-semibold my-20">{{ count }}</p>
      <div class="space-x-4">
        <button class="btn" @click="decrement">-</button>
        <button class="btn" @click="increment">+</button>
      </div>
    </div>
  </div>
</template>

<style scoped>
.btn {
  @apply px-4 py-3 rounded-lg border border-gray-500 font-medium w-14 focus:ring select-none;
}
</style>
