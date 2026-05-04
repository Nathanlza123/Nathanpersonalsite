<script setup lang="ts">
// 页脚组件，简洁收尾
</script>

<template>
  <footer class="contact-footer">
    <div class="container">
      <p class="footer-text">
        感谢你的到访。成长是一场漫长的旅程，愿你也能在路上找到自己的答案。
      </p>
      <div class="divider"></div>
      <p class="copyright">
        © {{ new Date().getFullYear() }} Nathan Li. 在觉察中成长。
      </p>
    </div>
  </footer>
</template>

<style scoped>
.contact-footer {
  padding: 4rem 2rem;
  background: linear-gradient(180deg, #0a0a1a 0%, #050510 100%);
  color: #fff;
  text-align: center;
}

.container {
  max-width: 600px;
  margin: 0 auto;
}

.footer-text {
  font-size: 1.1rem;
  line-height: 1.8;
  color: rgba(255, 255, 255, 0.75);
  margin: 0 0 2rem;
}

.divider {
  width: 60px;
  height: 3px;
  background: linear-gradient(to right, #00d4ff, #7b2ff7);
  border-radius: 2px;
  margin: 0 auto 2rem;
}

.copyright {
  font-size: 0.875rem;
  color: rgba(255, 255, 255, 0.4);
  margin: 0;
}

@media (max-width: 768px) {
  .contact-footer {
    padding: 3rem 1.5rem;
  }

  .footer-text {
    font-size: 1rem;
  }
}
</style>
