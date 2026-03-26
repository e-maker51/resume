<template>
  <div class="home">
    <div class="main-layout">
      <!-- 全局侧边栏 -->
      <ProfileSidebar />
      
      <!-- 主内容区 -->
      <main class="main-content">
        <EducationSection />
        <AboutHeroSection />
        <ProjectsSection />
        <Honorskill />
        <ExperienceSection />
      </main>
    </div>
  </div>
</template>

<script setup>
import ProfileSidebar from '../components/ProfileSidebar.vue'
import AboutHeroSection from '../components/AboutHeroSection.vue'
import EducationSection from '../components/EducationSection.vue'
import ProjectsSection from '../components/ProjectsSection.vue'
import Honorskill from '../components/Honorskill.vue'
import ExperienceSection from '../components/ExperienceSection.vue'
</script>

<style scoped>
.home {
  padding-top: var(--header-height);
}

.main-layout {
  display: grid;
  grid-template-columns: 320px 1fr;
  gap: var(--spacing-xxl);
  max-width: 1400px;
  margin: 0 auto;
  padding: var(--spacing-xl) var(--spacing-lg);
  align-items: start;
}

.main-content {
  display: flex;
  flex-direction: column;
  gap: var(--spacing-xl);
  min-height: calc(100vh - var(--header-height) - var(--spacing-xl) * 2);
}

/* 响应式 */
@media (max-width: 992px) {
  .main-layout {
    grid-template-columns: 1fr;
    gap: var(--spacing-xl);
  }
}
</style>
