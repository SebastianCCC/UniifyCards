<script setup>
const props = defineProps({
  CardTitle: String,
})
</script>

<template>
  <h2 class="uppercase">{{ CardTitle }}</h2>
</template>
