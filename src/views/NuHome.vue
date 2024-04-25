<script setup>
import HomeHeader from '@/components/HomeHeader.vue';
import BioCard from '@/components/BioCard.vue';
import ExpCard from '@/components/ExpCard.vue';
import LinksCard from '@/components/LinksCard.vue';
import PortfolioCard from '@/components/PortfolioCard.vue';
import SkillsCard from '@/components/SkillsCard.vue';
</script>

<template>
  <main>
    <HomeHeader />
    <section class="tile-card-wrapper">
      <BioCard />
      <PortfolioCard />
      <ExpCard />
      <SkillsCard />
      <LinksCard />
    </section>
  </main>
</template>
