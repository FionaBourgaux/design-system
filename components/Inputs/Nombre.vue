<script setup>
defineProps({
  modelValue: {
    type: Number,
    required: true,
  },
  name: {
    type: String,
    required: true,
  },
  min: {
    type: Number,
    required: null,
    default: null,
  },

  max: {
    type: Number,
    required: null,
    default: null,
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
    type="number"
    :min="min"
    :max="max"
    class="ring-2 ring-gray-200/75 focus:ring-gray-100 focus:outline-none focus:ring-2 px-4 py-2 w-full bg-black/50 text-gray-100"
  />
</template>
