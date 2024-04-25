<script setup>
defineProps({
  iconSrc: { type: String, default: null },
});
</script>

<template>
  <div class="logo-icon-wrapper">
    <img :src="iconSrc" />
  </div>
</template>
