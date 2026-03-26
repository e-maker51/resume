<template>
  <footer class="footer" id="contact">
    <div class="container">
      <div class="footer-content">
        <div class="footer-section">
          <h4 class="footer-title">联系方式</h4>
          <div class="contact-info">
            <a href="#" class="contact-item copyable" @click.prevent="copyToClipboard('zhangcheng_1631128@163.com', $event)" title="点击复制邮箱">
              <svg class="icon" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                <path d="M4 4h16c1.1 0 2 .9 2 2v12c0 1.1-.9 2-2 2H4c-1.1 0-2-.9-2-2V6c0-1.1.9-2 2-2z"></path>
                <polyline points="22,6 12,13 2,6"></polyline>
              </svg>
              邮箱：zhangcheng_1631128@163.com
            </a>
            <a href="#" class="contact-item copyable" @click.prevent="copyToClipboard('19583576278', $event)" title="点击复制电话">
              <svg class="icon" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                <path d="M22 16.92v3a2 2 0 0 1-2.18 2 19.79 19.79 0 0 1-8.63-3.07 19.5 19.5 0 0 1-6-6 19.79 19.79 0 0 1-3.07-8.67A2 2 0 0 1 4.11 2h3a2 2 0 0 1 2 1.72 12.84 12.84 0 0 0 .7 2.81 2 2 0 0 1-.45 2.11L8.09 9.91a16 16 0 0 0 6 6l1.27-1.27a2 2 0 0 1 2.11-.45 12.84 12.84 0 0 0 2.81.7A2 2 0 0 1 22 16.92z"></path>
              </svg>
              电话：19583576278
            </a>
            <div class="contact-item">
              <svg class="icon" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                <path d="M21 10c0 7-9 13-9 13s-9-6-9-13a9 9 0 0 1 18 0z"></path>
                <circle cx="12" cy="10" r="3"></circle>
              </svg>
              地址：四川省成都市
            </div>
          </div>
        </div>

        <div class="footer-section">
          <h4 class="footer-title">快速链接</h4>
          <div class="quick-links">
            <a href="#about" class="quick-link">简述</a>
            <a href="#education" class="quick-link">教育背景</a>
            <a href="#projects" class="quick-link">科研项目</a>
            <a href="#honors-skill" class="quick-link">荣誉技能</a>
            <a href="#experience" class="quick-link">实践经历</a>
          </div>
        </div>

        <div class="footer-section">
          <h4 class="footer-title">社交媒体</h4>
          <div class="social-links">
            <a href="https://github.com/e-maker51" target="_blank" rel="noopener noreferrer" class="social-link" aria-label="GitHub">
              <svg viewBox="0 0 24 24" fill="currentColor" width="20" height="20">
                <path d="M12 0c-6.626 0-12 5.373-12 12 0 5.302 3.438 9.8 8.207 11.387.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.084 1.839 1.237 1.839 1.237 1.07 1.834 2.807 1.304 3.492.997.107-.775.418-1.305.762-1.604-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23.957-.266 1.983-.399 3.003-.404 1.02.005 2.047.138 3.006.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.609-2.807 5.624-5.479 5.921.43.372.823 1.102.823 2.222v3.293c0 .319.192.694.801.576 4.765-1.589 8.199-6.086 8.199-11.386 0-6.627-5.373-12-12-12z"/>
              </svg>
            </a>
            <a href="https://gitee.com/e-maker" target="_blank" rel="noopener noreferrer" class="social-link" aria-label="Gitee">
              <svg viewBox="0 0 24 24" fill="currentColor" width="20" height="20">
                <path d="M11.984 0A12 12 0 0 0 0 12a12 12 0 0 0 12 12 12 12 0 0 0 12-12A12 12 0 0 0 12 0a12 12 0 0 0-.016 0zm6.09 5.333c.328 0 .593.266.593.593v1.778a.594.594 0 0 1-.593.593H9.481a.594.594 0 0 0-.593.593v9.481a.594.594 0 0 0 .593.593h1.778a.594.594 0 0 0 .593-.593v-3.852a.594.594 0 0 1 .593-.593h3.852a.594.594 0 0 0 .593-.593V9.481a.594.594 0 0 0-.593-.593h-3.852a.594.594 0 0 1-.593-.593V5.926c0-.327.265-.593.593-.593h8.593z"/>
              </svg>
            </a>
          </div>
        </div>
      </div>

      <div class="footer-bottom">
        <p class="copyright">
          &copy; {{ currentYear }} Zhang Cheng. All rights reserved.
        </p>
        <p class="credits">
          西南石油大学 · 计算机与软件学院 · 软件工程专业
        </p>
      </div>
    </div>
  </footer>

  <!-- 复制成功提示 -->
  <Teleport to="body">
    <Transition name="fade">
      <div v-if="copyTooltip.show" class="copy-tooltip" :style="{ left: copyTooltip.x + 'px', top: copyTooltip.y + 'px' }">
        {{ copyTooltip.text }}
      </div>
    </Transition>
  </Teleport>
</template>

<script setup>
import { computed, ref } from 'vue'

const currentYear = computed(() => new Date().getFullYear())

// 复制提示状态
const copyTooltip = ref({ show: false, text: '', x: 0, y: 0 })

// 复制到剪贴板
const copyToClipboard = async (text, event) => {
  try {
    await navigator.clipboard.writeText(text)
    showTooltip('已复制到剪贴板', event)
  } catch (err) {
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
</script>

<style scoped>
.footer {
  background-color: var(--color-bg-secondary);
  border-top: 1px solid var(--color-border);
  padding: var(--spacing-xl) 0 var(--spacing-md);
}

.footer-content {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: var(--spacing-lg);
  margin-bottom: var(--spacing-lg);
}

.footer-title {
  font-size: 1rem;
  font-weight: 600;
  margin-bottom: var(--spacing-sm);
  color: var(--color-text);
}

.contact-info {
  display: flex;
  flex-direction: column;
  gap: var(--spacing-xs);
}

.contact-item {
  display: flex;
  align-items: center;
  gap: var(--spacing-xs);
  color: var(--color-text-secondary);
  font-size: 0.9rem;
  transition: color var(--transition-fast);
}

.contact-item:hover {
  color: var(--color-primary);
}

.icon {
  width: 16px;
  height: 16px;
  flex-shrink: 0;
}

.quick-links {
  display: flex;
  flex-direction: column;
  gap: var(--spacing-xs);
}

.quick-link {
  color: var(--color-text-secondary);
  font-size: 0.9rem;
  transition: color var(--transition-fast);
}

.quick-link:hover {
  color: var(--color-primary);
}

.social-links {
  display: flex;
  gap: var(--spacing-sm);
}

.social-link {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 40px;
  height: 40px;
  border-radius: 50%;
  background-color: var(--color-bg);
  color: var(--color-text-secondary);
  transition: all var(--transition-fast);
}

.social-link:hover {
  background-color: var(--color-primary);
  color: white;
}

.footer-bottom {
  text-align: center;
  padding-top: var(--spacing-md);
  border-top: 1px solid var(--color-border);
}

.copyright {
  font-size: 0.875rem;
  color: var(--color-text-secondary);
  margin-bottom: var(--spacing-xs);
}

.credits {
  font-size: 0.8rem;
  color: var(--color-text-muted);
}

@media (max-width: 768px) {
  .footer-content {
    grid-template-columns: 1fr;
    gap: var(--spacing-md);
  }
}

/* 复制功能样式 */
.contact-item.copyable {
  cursor: pointer;
}

.contact-item.copyable:hover {
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
