<script setup>
import { computed } from 'vue';

const props = defineProps({
  hexCode: { type: String, default: null },
  progress: { type: Number, default: 0 },
  max: { type: Number, default: 0 },
});

const progressWidth = computed(() => {
  if (props.max === 0 || props.progress === 0) return 0;
  return (props.progress / props.max) * 100;
});

const innerStyle = computed(() => {
  let style = `width: ${progressWidth.value}%;`;
  if (!props.hexCode) return style;

  return (style += `background: ${props.hexCode}`);
});
</script>

<template>
  <div class="progress-bar-wrapper">
    <div class="progress-bar-full">
      <div class="progress-bar-inner" :style="innerStyle" />
    </div>
  </div>
</template>
