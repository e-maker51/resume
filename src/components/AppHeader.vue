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
      </nav>

      <button class="menu-toggle" @click="toggleMenu" aria-label="Toggle menu">
        <span class="menu-bar"></span>
        <span class="menu-bar"></span>
        <span class="menu-bar"></span>
      </button>
    </div>
  </header>
</template>

<script setup>
import { ref, onMounted, onUnmounted } from 'vue'

const isScrolled = ref(false)
const isMenuOpen = ref(false)

const navItems = [
  { label: '简述', href: '#about' },
  { label: '教育', href: '#education' },
  { label: '项目', href: '#projects' },
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
</style>
