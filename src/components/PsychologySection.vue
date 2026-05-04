<script setup lang="ts">
// 心理学常见模式板块，展示 4 个核心概念
import PatternCard from './PatternCard.vue';

const patterns = [
  {
    number: '01',
    title: 'INFP-大后期人格',
    description: 'INFP 是一种人格类型，倾向于内向、直觉、情感和知觉。J 代表判断型，意味着更喜欢结构化的生活方式。了解自己的类型，可以帮助我们更好地理解自己的行为模式和需求。',
    accentColor: '#00d4ff',
  },
  {
    number: '02',
    title: '盖勒普优势类型',
    description: 'Harmony，Empathy，Intellection，Consistency，Relator， Connectedness， Developer，Adaptability， Strategic， Discipline。是 Nathan 的核心优势',
    accentColor: '#7b2ff7',
  },
  {
    number: '03',
    title: '心理学爱好者',
    description: '有心理咨询的经历，由自己的经历出发，对CBT、ACT、精神分析等流派都有一些了解。心理学的视角帮助我更好地理解自己和他人，也让我意识到，很多困扰我们的模式，其实背后都有一些未被满足的需求。',
    accentColor: '#3b82f6',
  },
  {
    number: '04',
    title: 'Vide Coding 爱好者',
    description: '在不喜欢的工作中遇到了 Claude Code， 发现我在这个事情上面有着更长的注意力区间，正在这个可能是我的Soul Hobby 探索。',
    accentColor: '#a855f7',
  },
];
</script>

<template>
  <section class="psychology-section" id="patterns">
    <div class="container">
      <div class="section-header">
        <span class="section-label">心理学洞见</span>
        <h2 class="section-title">觉察那些常见的心理模式</h2>
        <p class="section-subtitle">
          这些模式藏在我们的日常反应中，觉察它们，是改变的开始
        </p>
      </div>
      <div class="cards-grid">
        <PatternCard
          v-for="pattern in patterns"
          :key="pattern.number"
          :number="pattern.number"
          :title="pattern.title"
          :description="pattern.description"
          :accent-color="pattern.accentColor"
        />
      </div>
    </div>
  </section>
</template>

<style scoped>
.psychology-section {
  padding: 6rem 2rem;
  background: linear-gradient(180deg, #0f172a 0%, #0a0a1a 100%);
}

.container {
  max-width: 1100px;
  margin: 0 auto;
}

.section-header {
  text-align: center;
  margin-bottom: 3.5rem;
}

.section-label {
  display: inline-block;
  font-size: 0.875rem;
  font-weight: 600;
  color: #00d4ff;
  text-transform: uppercase;
  letter-spacing: 2px;
  margin-bottom: 0.75rem;
}

.section-title {
  font-size: 2.25rem;
  font-weight: 700;
  color: #ffffff;
  margin: 0 0 1rem;
}

.section-subtitle {
  font-size: 1.1rem;
  color: rgba(255, 255, 255, 0.6);
  max-width: 500px;
  margin: 0 auto;
}

.cards-grid {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 1.5rem;
}

@media (max-width: 768px) {
  .psychology-section {
    padding: 4rem 1.5rem;
  }

  .section-title {
    font-size: 1.75rem;
  }

  .cards-grid {
    grid-template-columns: 1fr;
  }
}
</style>
