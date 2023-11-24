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
    class="text-[#001B79] hover:text-gray-100 underline transition"
  >
    <slot />
  </NuxtLink>
</template>
