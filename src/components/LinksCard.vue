<script setup>
import TileCard from '@/components/TileCard.vue';
import GithubLogo from '@/assets/icons/GithubLogo.vue';
import LinkedinLogo from '@/assets/icons/LinkedinLogo.vue';

const links = [
  {
    href: 'https://github.com/thewmking',
    component: GithubLogo
  },
  {
    href: 'https://www.linkedin.com/in/the-matthew-king/',
    component: LinkedinLogo
  }
];
</script>

<template>
  <TileCard title="Links">
    <template #body>
      <div class="icon-links">
        <a v-for="link in links" :href="link.href" :key="link.href" class="icon-link">
          <component :is="link.component" />
        </a>
      </div>
    </template>
  </TileCard>
</template>

<style>
.icon-links {
  display: flex;
  column-gap: 20px;
}

.icon-link {
  display: block;
  width: 75px;
}
</style>
