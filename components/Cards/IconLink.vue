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
    class="flex items-baseline space-x-8 p-4 group hover:bg-[#F8E8EE]/20 transition"
  >
    <div class="text-2xl text-[#F8E8EE] group-hover:text-[#001B79] group-hover:text-3xl transition">
      <slot name="icon" />
    </div>

    <div
      class="text-lg font-bold text-white group-hover:text-[#001B79] group-hover:text-2xl transition group-hover:font-titre"
    >
      <slot />
    </div>
  </NuxtLink>
</template>
