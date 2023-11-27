<script setup>
const isOpen = ref(false);
</script>

<template>
  <nav>
    <div
      class="flex md:flex-col items-center justify-between bg-[#1640D6] md:space-y-6 py-6 px-4 border-b border-white"
    >
      <div>
        <nuxt-link to="/">
          <slot name="logo"> </slot>
        </nuxt-link>
      </div>
      <div class="">
        <ul
          class="hidden md:flex items-center justify-between space-x-8 text-gray-300 text-xl"
        >
          <slot name="links"></slot>
        </ul>
        <ul class="flex md:hidden">
          <li class="">
            <button type="button" @click="isOpen = !isOpen">
              <i v-if="!isOpen" class="ri-menu-line text-3xl"></i>
              <i v-else class="ri-close-line text-4xl"></i>
            </button>
          </li>
        </ul>
      </div>
    </div>
    <div class="" v-if="isOpen">
      <ul
        class="md:hidden flex flex-col py-8 px-4 space-y-2 border-b border-white bg-gray-200/75 text-black transition-all text-xl"
      >
        <slot name="links"></slot>
      </ul>
    </div>
  </nav>
</template>
