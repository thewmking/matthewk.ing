<script setup>
import TileCard from '@/components/TileCard.vue';
</script>

<template>
  <TileCard title="Portfolio">
    <template #body>
      <ul>
        <li>
          <a href="https://github.com/thewmking/emerald">Emerald</a>: Vue SPA + Rails API backend
          monolith template
        </li>
        <li>
          <a href="https://thewmking.itch.io/dragon-attack">Dragon Attack</a>: 2D sidescroller demo
          game built with <a href="https://dragonruby.org/">DragonRuby</a> framework
        </li>
      </ul>
    </template>
  </TileCard>
</template>
