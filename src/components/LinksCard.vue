<script setup>
import TileCard from '@/components/TileCard.vue'
import GithubLogo from '@/assets/icons/GithubLogo.vue'
</script>

<template>
  <TileCard title="Links">
    <template #body>
      <a href="github.com/thewmking"><GithubLogo /></a>
      <div>linkedin</div>
    </template>
  </TileCard>
</template>
