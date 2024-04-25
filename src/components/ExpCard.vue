<script setup>
import TileCard from '@/components/TileCard.vue';
import LogoIcon from '@/components/LogoIcon.vue';

import assembleIcon from '@/assets/icons/assemble.png';
import launchlabsIcon from '@/assets/icons/launchlabs.png';
import sokalIcon from '@/assets/icons/sokal.png';
import webstreakIcon from '@/assets/icons/webstreak.png';

import ncsuIcon from '@/assets/icons/ncsu.png';
import odinIcon from '@/assets/icons/odin.png';

const expItems = [
  {
    name: 'Launch Labs',
    link: 'https://launchlabs.ai/',
    role: 'Senior Software Engineer',
    icon: launchlabsIcon,
    dates: '2024 - Present',
  },
  {
    name: 'ASMBL',
    link: 'https://assembleinc.com/',
    role: 'Software Engineer',
    icon: assembleIcon,
    dates: '2020-2024',
  },
  {
    name: 'Sokal',
    link: 'https://gosokal.com.com/',
    role: 'Software Development Manager',
    icon: sokalIcon,
    dates: '2019-2020',
  },
  {
    name: 'Webstreak (merged with Sokal)',
    role: 'Full Stack Developer',
    icon: webstreakIcon,
    dates: '2017-2019',
  },
];

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
  <TileCard title="Experience" class="exp-card-wrapper">
    <template #body>
      <h3>Positions:</h3>
      <ul class="experience-list">
        <li v-for="item in expItems" :key="item.name" class="exp-item">
          <LogoIcon :icon-src="item.icon" />
          <div class="exp-item-info">
            <a v-if="item.link" :href="item.link" class="exp-item-name">{{ item.name }}</a>
            <span v-if="!item.link" class="exp-item-name">{{ item.name }}</span>
            <span class="exp-item-role">{{ item.role }}</span>
            <span class="exp-item-dates">{{ item.dates }}</span>
          </div>
        </li>
      </ul>

      <h3>Education:</h3>
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
