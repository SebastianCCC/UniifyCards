<script setup>
const props = defineProps({
  CardValue: Number,
})
</script>

<template>
  <p class="text-lg">{{ CardValue }}</p>
</template>
