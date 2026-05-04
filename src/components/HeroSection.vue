<script setup lang="ts">
// 首屏组件，展示个人照片与核心标语
</script>

<template>
  <section class="hero-section">
    <div class="hero-content">
      <div class="photo-wrapper">
        <img src="/images/nathan-photo.png" alt="Nathan Li" class="photo" />
      </div>
      <div class="hero-text">
        <h1 class="name">Nathan Li</h1>
        <p class="tagline">在自我探索的路上，记录成长与觉察</p>
      </div>
    </div>
    <div class="scroll-hint">
      <span class="scroll-text">向下滚动</span>
      <div class="scroll-arrow"></div>
    </div>
  </section>
</template>

<style scoped>
.hero-section {
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  padding: 2rem;
  position: relative;
  background: linear-gradient(135deg, #0a0a1a 0%, #1a1a3a 50%, #0f172a 100%);
}

.hero-content {
  display: flex;
  align-items: center;
  gap: 3rem;
  max-width: 900px;
  animation: fadeInUp 0.8s ease-out;
}

@keyframes fadeInUp {
  from {
    opacity: 0;
    transform: translateY(30px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

.photo-wrapper {
  flex-shrink: 0;
}

.photo {
  width: 220px;
  height: 220px;
  border-radius: 50%;
  object-fit: cover;
  border: 2px solid rgba(255, 255, 255, 0.1);
  box-shadow:
    0 0 0 1px rgba(255, 255, 255, 0.05),
    0 20px 60px rgba(0, 212, 255, 0.15),
    0 0 80px rgba(123, 47, 247, 0.1);
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.photo:hover {
  transform: scale(1.05);
  box-shadow:
    0 0 0 1px rgba(255, 255, 255, 0.1),
    0 25px 70px rgba(0, 212, 255, 0.25),
    0 0 100px rgba(123, 47, 247, 0.15);
}

.hero-text {
  text-align: left;
}

.name {
  font-size: 3.5rem;
  font-weight: 700;
  color: #ffffff;
  margin: 0 0 1rem;
  letter-spacing: -1px;
  line-height: 1.1;
}

.tagline {
  font-size: 1.25rem;
  color: rgba(255, 255, 255, 0.7);
  margin: 0;
  font-weight: 400;
}

.scroll-hint {
  position: absolute;
  bottom: 2rem;
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 0.5rem;
  animation: bounce 2s infinite;
}

.scroll-text {
  font-size: 0.875rem;
  color: rgba(255, 255, 255, 0.4);
}

.scroll-arrow {
  width: 1px;
  height: 24px;
  background: linear-gradient(to bottom, #00d4ff, transparent);
}

@keyframes bounce {
  0%, 20%, 50%, 80%, 100% {
    transform: translateY(0);
  }
  40% {
    transform: translateY(-10px);
  }
  60% {
    transform: translateY(-5px);
  }
}

@media (max-width: 768px) {
  .hero-content {
    flex-direction: column;
    text-align: center;
    gap: 2rem;
  }

  .hero-text {
    text-align: center;
  }

  .name {
    font-size: 2.5rem;
  }

  .photo {
    width: 160px;
    height: 160px;
  }
}
</style>
