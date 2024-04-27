<script setup>
import TileCard from '@/components/TileCard.vue';
import LogoIcon from '@/components/LogoIcon.vue';

import ncsuIcon from '@/assets/icons/ncsu.png';
import odinIcon from '@/assets/icons/odin.png';

const edItems = [
  {
    name: 'NC State University',
    link: 'https://www.ncsu.edu/',
    program: 'Communication Media & Business Administration',
    icon: ncsuIcon,
    dates: '2009-2013',
  },
  {
    name: 'The Odin Project',
    link: 'https://www.theodinproject.com/',
    program: 'Full Stack Rails + JS Curriculum',
    icon: odinIcon,
    dates: '2016-2017',
  },
];
</script>

<template>
  <TileCard title="Education" class="exp-card-wrapper">
    <template #body>
      <ul class="experience-list">
        <li v-for="item in edItems" :key="item.name" class="exp-item">
          <LogoIcon :icon-src="item.icon" />
          <div class="exp-item-info">
            <a v-if="item.link" :href="item.link" class="exp-item-name">{{ item.name }}</a>
            <span v-if="!item.link" class="exp-item-name">{{ item.name }}</span>
            <span class="exp-item-role">{{ item.program }}</span>
            <span class="exp-item-dates">{{ item.dates }}</span>
          </div>
        </li>
      </ul>
    </template>
  </TileCard>
</template>
