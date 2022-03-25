<script setup>
const props = defineProps({
  CardStyle: String,
})
</script>

<template>
  <article class="p-6 m-3 rounded min-w-[250px]" :class="CardStyle">
    <slot></slot>
  </article>
</template>

<style scoped>
.bg-primary {
  background: #141e61;
  color: white;
}

.bg-light {
  background: #e8ebed;
}
</style>
