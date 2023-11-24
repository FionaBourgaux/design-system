<script setup>
defineProps({
  to: {
    type: String,
    required: true,
  },
});
</script>

<template>
  <NuxtLink
    :to="to"
    class="shadow-xl shadow-[#001B79]/50 bg-[#FF90C2] rounded-lg flex flex-col p-4 group hover:bg-gradient-to-r from-[#FF90C2] via-[#FDCEDF] to-[#FDCEDF] hover:transition-all transition items-center justify-center my-8 space-y-2 hover:scale-105"
  >
    <div class="text-5xl text-gray-400 group-hover:text-gray-800 transition">
      <slot name="icon" />
    </div>

    <div
      class="text-xl font-sans text-white group-hover:text-white"
    >
      <slot />
    </div>
  </NuxtLink>
</template>
