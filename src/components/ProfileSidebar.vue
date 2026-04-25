<template>
  <aside class="profile-sidebar">
    <div class="profile-card">
      <!-- 头像区域 -->
      <div class="profile-avatar">
        <img src="@/assets/p.png" alt="张程" class="profile-photo" />
      </div>

      <!-- 基础信息 - 四格排列 -->
      <div class="profile-info-grid">
        <div class="info-item">
          <span class="info-label">姓名</span>
          <span class="info-value">张程</span>
        </div>
        <div class="info-item">
          <span class="info-label">身份</span>
          <span class="info-value">本科生</span>
        </div>
        <div class="info-item">
          <span class="info-label">学校</span>
          <span class="info-value">西南石油大学</span>
        </div>
        <div class="info-item">
          <span class="info-label">地点</span>
          <span class="info-value">四川成都</span>
        </div>
      </div>

      <!-- 详细信息 -->
      <div class="profile-details">
        <div class="detail-row">
          <span class="detail-icon">
            <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" width="14" height="14">
              <path d="M22 10v6M2 10l10-5 10 5-10 5z"></path>
              <path d="M6 12v5c3 3 9 3 12 0v-5"></path>
            </svg>
          </span>
          <span class="detail-text">计算机与软件学院 · 软件工程</span>
        </div>
        <div class="detail-row">
          <span class="detail-icon">
            <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" width="14" height="14">
              <rect x="3" y="4" width="18" height="18" rx="2" ry="2"></rect>
              <line x1="16" y1="2" x2="16" y2="6"></line>
              <line x1="8" y1="2" x2="8" y2="6"></line>
              <line x1="3" y1="10" x2="21" y2="10"></line>
            </svg>
          </span>
          <span class="detail-text">2004年5月</span>
        </div>
      </div>

      <!-- 快速统计 -->
      <div class="profile-stats">
        <div class="stat-box clickable" @click="openModal('绩点和排名证明', 绩点和排名)">
          <span class="stat-value">4.15</span>
          <span class="stat-label">GPA</span>
          <div class="hover-tooltip">点击查看详情</div>
        </div>
        <div class="stat-box clickable" @click="openModal('绩点和排名证明', 绩点和排名)">
          <span class="stat-value">5/158</span>
          <span class="stat-label">排名</span>
          <div class="hover-tooltip">点击查看详情</div>
        </div>
        <div class="stat-box clickable" @click="openModal('绩点和排名证明', 绩点和排名)">
          <span class="stat-value">3.1%</span>
          <span class="stat-label">前</span>
          <div class="hover-tooltip">点击查看详情</div>
        </div>
      </div>

      <!-- 研究方向 -->
      <div class="profile-section">
        <h3 class="section-title">研究与学习方向</h3>
        <div class="tag-list">
          <span class="tag">时序序列</span>
          <span class="tag">计算机视觉</span>
          <span class="tag">深度学习</span>
          <span class="tag">大模型与软件应用</span>
        </div>
      </div>

      <!-- 主要荣誉 -->
      <div class="profile-section">
        <h3 class="section-title">主要荣誉</h3>
        <ul class="honor-list">
          <li class="honor-item">
            <span class="honor-badge">国家级</span>
            <span class="honor-name">国家励志奖学金</span>
          </li>
          <li class="honor-item">
            <span class="honor-badge">国家级</span>
            <span class="honor-name">全国大学生数学建模竞赛二等奖</span>
          </li>
          <li class="honor-item">
            <span class="honor-badge">国家级</span>
            <span class="honor-name">蓝桥杯优秀奖</span>
          </li>
        </ul>
      </div>

      <!-- 快速导航 -->
      <div class="profile-section">
        <h3 class="section-title">快速导航</h3>
        <nav class="nav-list">
          <a 
            v-for="item in navItems" 
            :key="item.id"
            :href="item.href" 
            class="nav-item"
            :class="{ active: activeNav === item.id }"
            @click.prevent="handleNavClick(item.id)"
          >
            <span class="nav-indicator"></span>
            <span class="nav-text">{{ item.label }}</span>
          </a>
        </nav>
      </div>

      <!-- 联系方式 -->
      <div class="profile-section">
        <h3 class="section-title">联系方式</h3>
        <div class="contact-list">
          <a href="#" class="contact-item copyable" @click.prevent="copyToClipboard('zhangcheng_1631128@163.com', $event)" title="点击复制邮箱">
            <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" width="16" height="16">
              <path d="M4 4h16c1.1 0 2 .9 2 2v12c0 1.1-.9 2-2 2H4c-1.1 0-2-.9-2-2V6c0-1.1.9-2 2-2z"></path>
              <polyline points="22,6 12,13 2,6"></polyline>
            </svg>
            <span>zhangcheng_1631128@163.com</span>
            <svg class="copy-icon" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" width="12" height="12">
              <rect x="9" y="9" width="13" height="13" rx="2" ry="2"></rect>
              <path d="M5 15H4a2 2 0 0 1-2-2V4a2 2 0 0 1 2-2h9a2 2 0 0 1 2 2v1"></path>
            </svg>
          </a>
          <a href="https://github.com/e-maker51" target="_blank" rel="noopener noreferrer" class="contact-item">
            <svg viewBox="0 0 24 24" fill="currentColor" width="16" height="16">
              <path d="M12 0c-6.626 0-12 5.373-12 12 0 5.302 3.438 9.8 8.207 11.387.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.084 1.839 1.237 1.839 1.237 1.07 1.834 2.807 1.304 3.492.997.107-.775.418-1.305.762-1.604-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23.957-.266 1.983-.399 3.003-.404 1.02.005 2.047.138 3.006.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.609-2.807 5.624-5.479 5.921.43.372.823 1.102.823 2.222v3.293c0 .319.192.694.801.576 4.765-1.589 8.199-6.086 8.199-11.386 0-6.627-5.373-12-12-12z"/>
            </svg>
            <span>GitHub</span>
          </a>
        </div>
      </div>

      <!-- 下载简历 -->
      <div class="profile-footer">
        <a :href="resumePdf" download="张程-简历.pdf" class="download-btn">
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" width="18" height="18">
            <path d="M21 15v4a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2v-4"></path>
            <polyline points="7 10 12 15 17 10"></polyline>
            <line x1="12" y1="15" x2="12" y2="3"></line>
          </svg>
          下载简历
        </a>
      </div>
    </div>
  </aside>

  <!-- 复制成功提示 -->
  <Teleport to="body">
    <Transition name="fade">
      <div v-if="copyTooltip.show" class="copy-tooltip" :style="{ left: copyTooltip.x + 'px', top: copyTooltip.y + 'px' }">
        {{ copyTooltip.text }}
      </div>
    </Transition>
  </Teleport>

  <!-- 证明材料弹窗 -->
  <CertificateModal
    v-model:visible="modalVisible"
    :title="modalTitle"
    :image-src="modalImageSrc"
  />
</template>

<script setup>
import { ref, onMounted, onUnmounted } from 'vue'
import CertificateModal from '../portfolio/CertificateModal.vue'

// 导入证书图片
import 绩点和排名 from '../assets/绩点和排名.png'
// 导入简历PDF
import resumePdf from '../assets/简历.pdf'

// 弹窗状态
const modalVisible = ref(false)
const modalTitle = ref('')
const modalImageSrc = ref('')

const openModal = (title, imageSrc) => {
  modalTitle.value = title
  modalImageSrc.value = imageSrc
  modalVisible.value = true
}

// 复制提示状态
const copyTooltip = ref({ show: false, text: '', x: 0, y: 0 })

// 复制到剪贴板
const copyToClipboard = async (text, event) => {
  try {
    await navigator.clipboard.writeText(text)
    showTooltip('已复制到剪贴板', event)
  } catch (err) {
    // 降级方案
    const textarea = document.createElement('textarea')
    textarea.value = text
    textarea.style.position = 'fixed'
    textarea.style.opacity = '0'
    document.body.appendChild(textarea)
    textarea.select()
    document.execCommand('copy')
    document.body.removeChild(textarea)
    showTooltip('已复制到剪贴板', event)
  }
}

// 显示提示
const showTooltip = (text, event) => {
  copyTooltip.value = {
    show: true,
    text,
    x: event.clientX,
    y: event.clientY - 40
  }
  setTimeout(() => {
    copyTooltip.value.show = false
  }, 2000)
}

// 导航项配置
const navItems = [
  { id: 'education', label: '教育背景', href: '#education' },
  { id: 'about', label: '简述', href: '#about' },
  { id: 'projects', label: '科研竞赛', href: '#projects' },
  { id: 'honors-skill', label: '荣誉技能', href: '#honors-skill' },
  { id: 'experience', label: '实践', href: '#experience' }
]

// 当前激活的导航项
const activeNav = ref('about')

// 处理导航点击
const handleNavClick = (id) => {
  activeNav.value = id
  const element = document.getElementById(id)
  if (element) {
    const headerHeight = parseInt(getComputedStyle(document.documentElement).getPropertyValue('--header-height')) || 64
    const elementPosition = element.getBoundingClientRect().top + window.pageYOffset
    const offsetPosition = elementPosition - headerHeight - 20
    
    window.scrollTo({
      top: offsetPosition,
      behavior: 'smooth'
    })
  }
}

// 监听滚动，更新当前激活的导航项
const handleScroll = () => {
  const headerHeight = parseInt(getComputedStyle(document.documentElement).getPropertyValue('--header-height')) || 64
  const scrollPosition = window.pageYOffset + headerHeight + 100

  // 从后往前查找，找到第一个在当前滚动位置上方的 section
  for (let i = navItems.length - 1; i >= 0; i--) {
    const element = document.getElementById(navItems[i].id)
    if (element) {
      const elementTop = element.getBoundingClientRect().top + window.pageYOffset
      if (scrollPosition >= elementTop) {
        activeNav.value = navItems[i].id
        break
      }
    }
  }
}

// 使用 IntersectionObserver 进行更精确的定位
let observer = null

onMounted(() => {
  // 初始化时检查当前位置
  handleScroll()
  
  // 监听滚动事件
  window.addEventListener('scroll', handleScroll, { passive: true })
  
  // 使用 IntersectionObserver 进行更精确的定位
  observer = new IntersectionObserver(
    (entries) => {
      entries.forEach((entry) => {
        if (entry.isIntersecting) {
          activeNav.value = entry.target.id
        }
      })
    },
    {
      rootMargin: '-20% 0px -60% 0px',
      threshold: 0
    }
  )
  
  // 观察所有 section
  navItems.forEach((item) => {
    const element = document.getElementById(item.id)
    if (element) {
      observer.observe(element)
    }
  })
})

onUnmounted(() => {
  window.removeEventListener('scroll', handleScroll)
  if (observer) {
    observer.disconnect()
  }
})
</script>

<style scoped>
.profile-sidebar {
  position: sticky;
  top: calc(var(--header-height) + var(--spacing-lg));
  height: calc(100vh - var(--header-height) - var(--spacing-xl));
  overflow-y: auto;
  padding-right: 4px;
  padding-top: 2px;
  padding-bottom: 2px;
}

.profile-sidebar::-webkit-scrollbar {
  width: 6px;
}

.profile-sidebar::-webkit-scrollbar-track {
  background: transparent;
  margin: 12px 0;
}

.profile-sidebar::-webkit-scrollbar-thumb {
  background: var(--color-border);
  border-radius: 3px;
  margin: 12px 0;
}

.profile-card {
  background: var(--color-bg);
  border-left: 3px solid var(--color-primary);
  background: linear-gradient(to right, rgba(59, 130, 246, 0.03), transparent);
  border: 1px solid var(--color-border);
 border-radius: 8px;
  padding: var(--spacing-md);
  box-shadow: 0 1px 3px rgba(0, 0, 0, 0.06);
  transition: all var(--transition-fast);
}

.profile-card:hover {
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.08);
  border-color: var(--color-primary);
  transform: translateY(-2px);
}

/* 头像 - 缩小并上移 */
.profile-avatar {
  text-align: center;
  margin-top: -10px;
  margin-bottom: var(--spacing-sm)-6px;
}

.profile-photo {
  width: 110px;
  height: 110px;
  border-radius: 50%;
  object-fit: cover;
  border: 3px solid var(--color-bg);
  box-shadow: 0 4px 16px rgba(0, 54, 159, 0.2);
  transition: transform var(--transition-normal), box-shadow var(--transition-normal);
}

.profile-photo:hover {
  transform: scale(1.03);
  box-shadow: 0 6px 24px rgba(0, 54, 159, 0.3);
}

/* 基础信息 - 四格排列 */
.profile-info-grid {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 1px;
  background: var(--color-border);
  border-radius: 12px;
  overflow: hidden;
  margin-bottom: var(--spacing-md);
}

.info-item {
  background: var(--color-bg);
  padding: 12px 8px;
  text-align: center;
  display: flex;
  flex-direction: column;
  gap: 4px;
}

.info-label {
  font-size: 0.7rem;
  color: var(--color-text-muted);
  text-transform: uppercase;
  letter-spacing: 0.5px;
}

.info-value {
  font-size: 0.85rem;
  font-weight: 600;
  color: var(--color-text);
}

/* 详细信息 */
.profile-details {
  margin-bottom: var(--spacing-md);
  padding-bottom: var(--spacing-md);
  border-bottom: 1px solid var(--color-border);
}

.detail-row {
  display: flex;
  align-items: center;
  gap: 8px;
  font-size: 0.8rem;
  color: var(--color-text-secondary);
  margin-bottom: 6px;
}

.detail-row:last-child {
  margin-bottom: 0;
}

.detail-icon {
  color: var(--color-primary);
  display: flex;
  align-items: center;
}

/* 快速统计 */
.profile-stats {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: var(--spacing-sm);
  margin-bottom: var(--spacing-md);
  padding-bottom: var(--spacing-md);
  border-bottom: 1px solid var(--color-border);
}

.stat-box {
  text-align: center;
  padding: 10px 4px;
  background: var(--color-bg);
  border-radius: 8px;
  border: 1px solid var(--color-border);
  transition: all var(--transition-fast);
  position: relative;
}

.stat-box:hover {
  border-color: var(--color-primary);
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.06);
}

.stat-box.clickable {
  cursor: pointer;
}

.stat-box.clickable:hover {
  background: linear-gradient(to bottom, rgba(59, 130, 246, 0.05), transparent);
  transform: translateY(-2px);
}

.stat-value {
  display: block;
  font-size: 1.1rem;
  font-weight: 700;
  color: var(--color-primary);
  line-height: 1.2;
}

.stat-label {
  font-size: 0.7rem;
  color: var(--color-text-muted);
}

/* 悬浮提示 - 样式与按钮一致 */
.hover-tooltip {
  position: absolute;
  left: 50%;
  bottom: 100%;
  transform: translateX(-50%) translateY(-8px);
  padding: 0.25rem 0.625rem;
  font-size: 0.75rem;
  font-weight: 600;
  color: var(--color-primary);
  background: rgba(59, 130, 246, 0.1);
  border-radius: 4px;
  white-space: nowrap;
  opacity: 0;
  visibility: hidden;
  transition: all 0.2s ease;
  pointer-events: none;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
}

.hover-tooltip::after {
  content: '';
  position: absolute;
  top: 100%;
  left: 50%;
  transform: translateX(-50%);
  border: 4px solid transparent;
  border-top-color: rgba(59, 130, 246, 0.1);
}

.stat-box.clickable:hover .hover-tooltip {
  opacity: 1;
  visibility: visible;
  transform: translateX(-50%) translateY(-4px);
}

/* 通用区块 */
.profile-section {
  margin-bottom: var(--spacing-md);
  padding-bottom: var(--spacing-md);
  border-bottom: 1px solid var(--color-border);
}

.profile-section:last-of-type {
  border-bottom: none;
  margin-bottom: 0;
}

.section-title {
  font-size: 0.8rem;
  font-weight: 600;
  color: var(--color-text);
  text-transform: uppercase;
  letter-spacing: 0.5px;
  margin-bottom: 10px;
}

/* 研究方向标签 */
.tag-list {
  display: flex;
  flex-wrap: wrap;
  gap: 6px;
}

.tag {
  display: inline-block;
  padding: 4px 10px;
  font-size: 0.75rem;
  background: var(--color-bg-secondary);
  color: var(--color-text-secondary);
  border-radius: 4px;
  border: 1px solid var(--color-border);
}

/* 荣誉列表 */
.honor-list {
  list-style: none;
  display: flex;
  flex-direction: column;
  gap: 8px;
}

.honor-item {
  display: flex;
  align-items: center;
  gap: 8px;
  font-size: 0.8rem;
}

.honor-badge {
  display: inline-block;
  padding: 2px 6px;
  font-size: 0.65rem;
  font-weight: 600;
  background: var(--color-primary);
  color: white;
  border-radius: 3px;
  white-space: nowrap;
}

.honor-name {
  color: var(--color-text-secondary);
}

/* 快速导航 - 带蓝色指示条 */
.nav-list {
  display: flex;
  flex-direction: column;
  gap: 4px;
}

.nav-item {
  display: flex;
  align-items: center;
  gap: 10px;
  padding: 10px 12px;
  font-size: 0.85rem;
  color: var(--color-text-secondary);
  border-radius: 8px;
  transition: all var(--transition-fast);
  position: relative;
  cursor: pointer;
}

.nav-indicator {
  width: 3px;
  height: 16px;
  background: transparent;
  border-radius: 2px;
  transition: all var(--transition-fast);
  flex-shrink: 0;
}

.nav-text {
  transition: all var(--transition-fast);
}

.nav-item:hover {
  background: var(--color-bg-secondary);
  color: var(--color-text);
}

.nav-item:hover .nav-indicator {
  background: var(--color-border);
}

.nav-item.active {
  background: rgba(0, 54, 159, 0.08);
  color: var(--color-primary);
}

.nav-item.active .nav-indicator {
  background: var(--color-primary);
  box-shadow: 0 0 8px rgba(0, 54, 159, 0.4);
}

/* 联系方式 */
.contact-list {
  display: flex;
  flex-direction: column;
  gap: 8px;
}

.contact-item {
  display: flex;
  align-items: center;
  gap: 8px;
  padding: 8px 10px;
  font-size: 0.75rem;
  color: var(--color-text-secondary);
  background: var(--color-bg-secondary);
  border-radius: 6px;
  transition: all var(--transition-fast);
  overflow: hidden;
}

.contact-item svg {
  flex-shrink: 0;
  color: var(--color-primary);
}

.contact-item span {
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
}

.contact-item:hover {
  background: var(--color-primary);
  color: white;
}

.contact-item:hover svg {
  color: white;
}

/* 下载按钮 */
.profile-footer {
  margin-top: 0;
  padding-top: var(--spacing-md);
}

.download-btn {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 8px;
  width: 100%;
  padding: 12px;
  font-size: 0.85rem;
  font-weight: 500;
  color: white;
  background: var(--color-primary);
  border-radius: 8px;
  transition: all var(--transition-fast);
}

.download-btn:hover {
  background: var(--color-primary-light);
  transform: translateY(-2px);
  box-shadow: 0 4px 12px rgba(0, 54, 159, 0.3);
}

/* 响应式 */
@media (max-width: 992px) {
  .profile-sidebar {
    position: static;
    height: auto;
    overflow-y: visible;
  }

  .profile-card {
    display: grid;
    grid-template-columns: 140px 1fr;
    gap: var(--spacing-lg);
    align-items: start;
  }

  .profile-avatar {
    margin-top: 0;
    margin-bottom: 0;
  }

  .profile-photo {
    width: 100px;
    height: 100px;
  }

  .profile-info-grid {
    margin-bottom: var(--spacing-sm);
  }

  .profile-details {
    margin-bottom: var(--spacing-sm);
    padding-bottom: var(--spacing-sm);
  }

  .profile-stats {
    margin-bottom: var(--spacing-sm);
    padding-bottom: var(--spacing-sm);
  }

  .profile-section {
    margin-bottom: var(--spacing-sm);
    padding-bottom: var(--spacing-sm);
  }

  .profile-footer {
    margin-top: var(--spacing-sm);
    padding-top: var(--spacing-sm);
  }
  
  .nav-item {
    padding: 8px 10px;
  }
}

@media (max-width: 576px) {
  .profile-card {
    grid-template-columns: 1fr;
    text-align: center;
  }

  .profile-photo {
    width: 100px;
    height: 100px;
  }

  .detail-row {
    justify-content: center;
  }

  .honor-item {
    justify-content: center;
  }

  .contact-item {
    justify-content: center;
  }
  
  .nav-item {
    justify-content: center;
  }
}

/* 复制功能样式 */
.contact-item.copyable {
  cursor: pointer;
  position: relative;
}

.contact-item.copyable:hover {
  background: rgba(59, 130, 246, 0.05);
}

.copy-icon {
  margin-left: auto;
  opacity: 0.6;
  transition: opacity 0.2s ease;
}

.contact-item.copyable:hover .copy-icon {
  opacity: 1;
  color: var(--color-primary);
}

/* 复制提示 */
.copy-tooltip {
  position: fixed;
  background: var(--color-primary);
  color: white;
  padding: 8px 16px;
  border-radius: 6px;
  font-size: 0.85rem;
  font-weight: 500;
  z-index: 9999;
  pointer-events: none;
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.15);
  transform: translateX(-50%);
}

.copy-tooltip::after {
  content: '';
  position: absolute;
  top: 100%;
  left: 50%;
  transform: translateX(-50%);
  border: 6px solid transparent;
  border-top-color: var(--color-primary);
}

/* 提示动画 */
.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.3s ease, transform 0.3s ease;
}

.fade-enter-from,
.fade-leave-to {
  opacity: 0;
  transform: translateX(-50%) translateY(-10px);
}
</style>
