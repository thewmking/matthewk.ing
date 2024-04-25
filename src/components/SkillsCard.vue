<script setup>
import TileCard from '@/components/TileCard.vue';
import LogoIcon from '@/components/LogoIcon.vue';
import ProgressBar from '@/components/ProgressBar.vue';

import awsIcon from '@/assets/icons/aws.png';
import cssIcon from '@/assets/icons/css.png';
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
    hex: '#a70900',
  },
  {
    name: 'Ruby on Rails',
    score: 5,
    icon: railsIcon,
    hex: '#cc0000',
  },
  {
    name: 'Javascript',
    score: 5,
    icon: jsIcon,
    hex: '#f1dc4e',
  },
  {
    name: 'Vue.js',
    score: 5,
    icon: vueIcon,
    hex: '#41b883',
  },
  {
    name: 'CSS',
    score: 5,
    icon: cssIcon,
    hex: '#2465f2',
  },
  {
    name: 'PostgreSQL',
    score: 4,
    icon: postgresIcon,
    hex: '#306793',
  },
  {
    name: 'AWS',
    score: 3.5,
    icon: awsIcon,
    hex: '#ff9a01',
  },
  {
    name: 'React JS',
    score: 3,
    icon: reactIcon,
    hex: '#61dbfc',
  },
  {
    name: 'nginx',
    score: 3,
    icon: nginxIcon,
    hex: '#049535',
  },
];
</script>

<template>
  <TileCard title="Skills">
    <template #body>
      <ul class="skills-list">
        <li v-for="item in skillItems" :key="item.name" class="skill-item">
          <LogoIcon :icon-src="item.icon" />
          <div class="skill-item-info">
            <span class="skill-item-name">{{ item.name }}</span>
            <div class="skill-item-score">
              <ProgressBar :max="5" :progress="item.score" :hex-code="item.hex" />
            </div>
          </div>
        </li>
      </ul>
    </template>
  </TileCard>
</template>
