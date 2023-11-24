<script setup>
const props = defineProps({
  to: {
    type: String,
    required: true,
  },
});
</script>

<template>
  <NuxtLink
    :to="to"
    class="text-lg text-bold text-white hover:text-[#FF90C2] font-sans "
    active-class=""
  >
    <slot />
  </NuxtLink>
</template>
