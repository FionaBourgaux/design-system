<script setup>
defineProps({
  modelValue: {
    type: String,
    required: true,
  },
  name: {
    type: String,
    required: true,
  },
});
const emit = defineEmits(["update:modelValue"]);

const handleChange = (event) => {
  emit("update:modelValue", event.target.value);
};
</script>

<template>
  <input
    :name="name"
    :id="name"
    :value="modelValue"
    @input="handleChange"
    type="email"
    class="ring-2 ring-gray-200/75 focus:ring-gray-100 focus:outline-none focus:ring-2 px-4 py-2 w-full bg-black/50 text-gray-100"
  />
</template>
