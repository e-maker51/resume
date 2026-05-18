<template>
  <header class="header" :class="{ 'header-scrolled': isScrolled }">
    <div class="container header-container">
      <a href="#" class="logo">
        <img src="@/assets/简历.svg" alt="简历" class="logo-icon" />
        <div class="logo-text-wrapper">
          <span class="logo-text">张程</span>
          <span class="logo-subtitle">Zhang Cheng</span>
        </div>
      </a>

      <nav class="nav" :class="{ 'nav-open': isMenuOpen }">
        <a
          v-for="item in navItems"
          :key="item.href"
          :href="item.href"
          class="nav-link"
          @click="closeMenu"
        >
          {{ item.label }}
        </a>
        <button class="nav-link demo-btn" @click="openDemoModal">
          项目演示
        </button>
      </nav>

      <button class="menu-toggle" @click="toggleMenu" aria-label="Toggle menu">
        <span class="menu-bar"></span>
        <span class="menu-bar"></span>
        <span class="menu-bar"></span>
      </button>
    </div>
  </header>

  <!-- 项目演示弹窗 -->
  <Teleport to="body">
    <div v-if="isDemoModalOpen" class="demo-modal-overlay" @click="closeDemoModal">
      <div class="demo-modal" @click.stop>
        <div class="demo-modal-header">
          <h2 class="demo-modal-title">项目演示</h2>
          <button class="demo-modal-close" @click="closeDemoModal" aria-label="关闭">
            <span class="close-icon">×</span>
          </button>
        </div>
        <div class="demo-modal-content">
          <div class="demo-projects-grid">
            <div class="demo-project-card">
              <div class="demo-project-placeholder">
                <span class="demo-placeholder-text">敬请期待</span>
              </div>
              <h3 class="demo-project-name">全天候车牌识别系统</h3>
            </div>
            <div class="demo-project-card">
              <div class="demo-project-placeholder">
                <span class="demo-placeholder-text">敬请期待</span>
              </div>
              <h3 class="demo-project-name">果卜坡地质形变预测</h3>
            </div>
            <div class="demo-project-card">
              <div class="demo-project-placeholder">
                <span class="demo-placeholder-text">敬请期待</span>
              </div>
              <h3 class="demo-project-name">船舶维修领域智能问答系统</h3>
            </div>
          </div>
        </div>
      </div>
    </div>
  </Teleport>
</template>

<script setup>
import { ref, onMounted, onUnmounted } from 'vue'

const isScrolled = ref(false)
const isMenuOpen = ref(false)
const isDemoModalOpen = ref(false)

const navItems = [
  { label: '教育背景', href: '#education' },
  { label: '简述', href: '#about' },
  { label: '科研竞赛', href: '#projects' },
  { label: '荣誉技能', href: '#honors-skill' },
  { label: '实践', href: '#experience' },
  { label: '联系', href: '#contact' }
]

const handleScroll = () => {
  isScrolled.value = window.scrollY > 50
}

const toggleMenu = () => {
  isMenuOpen.value = !isMenuOpen.value
}

const closeMenu = () => {
  isMenuOpen.value = false
}

const openDemoModal = () => {
  isDemoModalOpen.value = true
  closeMenu()
}

const closeDemoModal = () => {
  isDemoModalOpen.value = false
}

onMounted(() => {
  window.addEventListener('scroll', handleScroll)
})

onUnmounted(() => {
  window.removeEventListener('scroll', handleScroll)
})
</script>

<style scoped>
.header {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  height: var(--header-height);
  background-color: var(--color-bg);
  border-bottom: 1px solid transparent;
  z-index: 1000;
  transition: all var(--transition-normal);
}

.header-scrolled {
  border-bottom-color: var(--color-border);
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.05);
}

.header-container {
  display: flex;
  align-items: center;
  justify-content: space-between;
  height: 100%;
}

.logo {
  display: flex;
  align-items: center;
  gap: 10px;
  text-decoration: none;
}

.logo-icon {
  width: 36px;
  height: 36px;
  object-fit: contain;
  border-radius: 6px;
  transition: transform 0.2s ease;
}

.logo:hover .logo-icon {
  transform: scale(1.05);
}

.logo-text-wrapper {
  display: flex;
  flex-direction: column;
}

.logo-text {
  font-size: 1.25rem;
  font-weight: 600;
  color: var(--color-text);
  line-height: 1.2;
}

.logo-subtitle {
  font-size: 0.75rem;
  color: var(--color-text-muted);
  font-weight: 400;
}

.nav {
  display: flex;
  gap: var(--spacing-lg);
}

.nav-link {
  color: var(--color-text-secondary);
  font-size: 0.9rem;
  font-weight: 500;
  padding: 0.5rem 0;
  position: relative;
  transition: color var(--transition-fast);
}

.nav-link::after {
  content: '';
  position: absolute;
  bottom: 0;
  left: 0;
  width: 0;
  height: 2px;
  background-color: var(--color-primary);
  transition: width var(--transition-fast);
}

.nav-link:hover {
  color: var(--color-primary);
}

.nav-link:hover::after {
  width: 100%;
}

.menu-toggle {
  display: none;
  flex-direction: column;
  gap: 5px;
  background: none;
  border: none;
  cursor: pointer;
  padding: 5px;
}

.menu-bar {
  display: block;
  width: 24px;
  height: 2px;
  background-color: var(--color-text);
  transition: all var(--transition-fast);
}

@media (max-width: 768px) {
  .nav {
    position: fixed;
    top: var(--header-height);
    left: 0;
    right: 0;
    background-color: var(--color-bg);
    flex-direction: column;
    padding: var(--spacing-md);
    gap: var(--spacing-sm);
    border-bottom: 1px solid var(--color-border);
    transform: translateY(-100%);
    opacity: 0;
    visibility: hidden;
    transition: all var(--transition-normal);
  }

  .nav-open {
    transform: translateY(0);
    opacity: 1;
    visibility: visible;
  }

  .menu-toggle {
    display: flex;
  }
}

/* 项目演示按钮样式 */
.demo-btn {
  background: none;
  border: none;
  cursor: pointer;
  font-family: inherit;
}

/* 项目演示弹窗样式 */
.demo-modal-overlay {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background-color: rgba(0, 0, 0, 0.6);
  backdrop-filter: blur(4px);
  z-index: 2000;
  display: flex;
  align-items: center;
  justify-content: center;
  padding: var(--spacing-md);
  animation: fadeIn 0.3s ease;
}

.demo-modal {
  background: var(--color-bg);
  border-left: 3px solid var(--color-primary);
  background: linear-gradient(to right, rgba(59, 130, 246, 0.03), transparent), var(--color-bg);
  border: 1px solid var(--color-border);
  border-radius: 8px;
  box-shadow: 0 20px 60px rgba(0, 0, 0, 0.3);
  width: 100%;
  max-width: 900px;
  max-height: 90vh;
  overflow: hidden;
  animation: slideUp 0.3s ease;
}

.demo-modal-header {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: var(--spacing-md) var(--spacing-lg);
  border-bottom: 1px solid var(--color-border);
  background: linear-gradient(to right, rgba(59, 130, 246, 0.05), transparent);
}

.demo-modal-title {
  font-size: 1.4rem;
  font-weight: 600;
  color: var(--color-text);
  margin: 0;
  padding-bottom: var(--spacing-xs);
  border-bottom: 2px solid var(--color-primary);
  display: inline-block;
  letter-spacing: 0.5px;
}

.demo-modal-close {
  background: var(--color-bg-secondary);
  border: 1px solid var(--color-border);
  cursor: pointer;
  padding: 0.5rem;
  border-radius: 6px;
  transition: all var(--transition-fast);
  display: flex;
  align-items: center;
  justify-content: center;
  width: 36px;
  height: 36px;
}

.demo-modal-close:hover {
  background-color: var(--color-primary);
  border-color: var(--color-primary);
  transform: translateY(-2px);
  box-shadow: 0 4px 12px rgba(59, 130, 246, 0.3);
}

.demo-modal-close:hover .close-icon {
  color: white;
}

.close-icon {
  font-size: 1.5rem;
  color: var(--color-text-secondary);
  line-height: 1;
  transition: color var(--transition-fast);
}

.demo-modal-content {
  padding: var(--spacing-lg);
  overflow-y: auto;
  max-height: calc(90vh - 80px);
  background: var(--color-bg);
}

.demo-projects-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
  gap: var(--spacing-lg);
}

.demo-project-card {
  background-color: var(--color-bg-secondary);
  border: 1px solid var(--color-border);
  border-radius: 8px;
  overflow: hidden;
  transition: all var(--transition-fast);
  box-shadow: 0 1px 3px rgba(0, 0, 0, 0.06);
}

.demo-project-card:hover {
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.08);
  border-color: var(--color-primary);
  transform: translateY(-2px);
}

.demo-project-placeholder {
  aspect-ratio: 16 / 10;
  background: linear-gradient(135deg, var(--color-bg) 0%, var(--color-bg-secondary) 100%);
  display: flex;
  align-items: center;
  justify-content: center;
  border-bottom: 1px solid var(--color-border);
  position: relative;
}

.demo-project-placeholder::before {
  content: '▶';
  position: absolute;
  font-size: 3rem;
  color: var(--color-primary);
  opacity: 0.3;
  transition: all var(--transition-fast);
}

.demo-project-card:hover .demo-project-placeholder::before {
  opacity: 0.6;
  transform: scale(1.1);
}

.demo-placeholder-text {
  font-size: 1.1rem;
  font-weight: 500;
  color: var(--color-text-muted);
  letter-spacing: 2px;
  z-index: 1;
  background: rgba(255, 255, 255, 0.8);
  padding: 0.5rem 1rem;
  border-radius: 4px;
  backdrop-filter: blur(4px);
}

.demo-project-name {
  font-size: 1rem;
  font-weight: 600;
  color: var(--color-text);
  padding: var(--spacing-md);
  margin: 0;
  text-align: center;
  background: var(--color-bg-secondary);
  border-top: 1px solid var(--color-border);
}

@keyframes fadeIn {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}

@keyframes slideUp {
  from {
    opacity: 0;
    transform: translateY(30px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

@media (max-width: 768px) {
  .demo-modal {
    max-width: 100%;
    max-height: 95vh;
  }

  .demo-projects-grid {
    grid-template-columns: 1fr;
  }

  .demo-modal-title {
    font-size: 1.25rem;
  }
}
</style>
