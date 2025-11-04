<template>
  <svg
    xmlns="http://www.w3.org/2000/svg"
    viewBox="0 0 24 24"
    fill="none"
    :width="size"
    :height="size"
    :stroke="color"
    stroke-width="2"
    stroke-linecap="round"
    stroke-linejoin="round"
  >
    <path d="M5 12h14" />
    <path d="m12 5 7 7-7 7" />
  </svg>
</template>

<script setup>
  const props = defineProps({
    size: {
      type: [Number, String],
      default: 24,
    },
    color: {
      type: String,
      default: "currentColor",
    },
  })
</script>
