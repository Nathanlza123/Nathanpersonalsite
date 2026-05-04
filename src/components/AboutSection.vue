<script setup lang="ts">
// 关于个人成长故事的板块
</script>

<template>
  <section class="about-section" id="about">
    <div class="container">
      <div class="section-header">
        <span class="section-label">关于我</span>
        <h2 class="section-title">成长，是一场持续的觉察</h2>
      </div>
      <div class="content">
        <div class="content-bar"></div>
        <div class="content-text">
          <p>
            这不是一个求职网站，是一个关于 Nathan Li，一个这个时间上独一无二的个体
            在人生漫漫三十年来，形成的人格和模式。
          </p>
          <p>
            接触心理学让我开始理解，很多困扰我们的情绪和行为，
            背后往往藏着一些我们自己都未曾察觉的模式。
            觉察，是改变的第一步。
          </p>
          <p>
            这个网站是我记录这段旅程的一个小角落。
            在这里，我分享关于自我成长的心得，也整理那些让我受益匪浅的洞见。
            希望它们也能为你带来一点启发。
          </p>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.about-section {
  padding: 6rem 2rem;
  background: linear-gradient(180deg, #0a0a1a 0%, #0f172a 100%);
}

.container {
  max-width: 800px;
  margin: 0 auto;
}

.section-header {
  text-align: center;
  margin-bottom: 3rem;
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
  margin: 0;
}

.content {
  display: flex;
  gap: 2rem;
}

.content-bar {
  width: 4px;
  background: linear-gradient(to bottom, #00d4ff, #7b2ff7);
  border-radius: 2px;
  flex-shrink: 0;
}

.content-text {
  display: flex;
  flex-direction: column;
  gap: 1.5rem;
}

.content-text p {
  font-size: 1.1rem;
  line-height: 1.8;
  color: rgba(255, 255, 255, 0.75);
}

@media (max-width: 768px) {
  .about-section {
    padding: 4rem 1.5rem;
  }

  .section-title {
    font-size: 1.75rem;
  }

  .content-bar {
    width: 3px;
  }
}
</style>
