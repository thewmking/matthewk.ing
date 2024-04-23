<script setup>
import TileCard from '@/components/TileCard.vue';
import SkillIcon from '@/components/SkillIcon.vue';

import awsIcon from '@/assets/icons/aws.png';
import jsIcon from '@/assets/icons/js.png';
import nginxIcon from '@/assets/icons/nginx.png';
import postgresIcon from '@/assets/icons/postgres.png';
import railsIcon from '@/assets/icons/rails.png';
import reactIcon from '@/assets/icons/react.png';
import rubyIcon from '@/assets/icons/ruby.png';
import vueIcon from '@/assets/icons/vue.png';

const skillItems = [
  {
    name: 'Ruby',
    score: 5,
    icon: rubyIcon,
    hex: '',
  },
  {
    name: 'Ruby on Rails',
    score: 5,
    icon: railsIcon,
    hex: '',
  },
  {
    name: 'Javascript',
    score: 5,
    icon: jsIcon,
    hex: '',
  },
  {
    name: 'Vue.js',
    score: 5,
    icon: vueIcon,
    hex: '',
  },
  {
    name: 'PostgreSQL',
    score: 4,
    icon: postgresIcon,
    hex: '',
  },
  {
    name: 'React JS',
    score: 3,
    icon: reactIcon,
    hex: '',
  },
  {
    name: 'AWS',
    score: 3,
    icon: awsIcon,
    hex: '',
  },
  {
    name: 'nginx',
    score: 3,
    icon: nginxIcon,
    hex: '',
  },
];
</script>

<template>
  <TileCard title="Skills">
    <template #body>
      <h3>Positions:</h3>
      <ul>
        <li v-for="item in skillItems" :key="item.name" class="skill-item">
          <SkillIcon :icon-src="item.icon" />
          <span class="skill-item-name">{{ item.name }}</span>
          <div class="skill-item-score">{{ item.score }}</div>
        </li>
      </ul>
    </template>
  </TileCard>
</template>
