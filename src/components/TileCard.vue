<script setup>
defineProps({
  title: { type: String, default: '' }
})
</script>

<template>
  <div class="tile-card">
    <h2 v-if="title" class="card-title">{{ title }}</h2>
    <slot name="body" />
  </div>
</template>
