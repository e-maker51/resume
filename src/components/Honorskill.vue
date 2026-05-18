<template>
  <section class="honors-skill-section" id="honors-skill">
    <!-- 荣誉奖项 -->
    <div class="content-section">
      <h3 class="section-title">荣誉奖项</h3>
      <div class="honors-container">
        <div class="honor-category">
          <h4 class="honor-category-title">
            <span class="category-icon">🏆</span>
            国家级奖项
          </h4>
          <ul class="honor-list">
            <li class="honor-item" @click="openModal('大学生训练计划国家级立项',国家级大学生创新创业训练计划)">
              <span class="honor-badge national">国家级</span>
              <span class="honor-name">大学生训练计划国家级立项</span>
              <div class="honor-actions">
                <button class="detail-btn" @click.stop="openModal('大学生训练计划国家级立项',国家级大学生创新创业训练计划)">
                  <span class="btn-text">详情</span>
                </button>
                <span class="honor-year">2025</span>
              </div>
              <div class="hover-tooltip">点击查看详情</div>
            </li>
            <li class="honor-item" @click="openModal('全国大学生数学建模竞赛二等奖', 全国大学生建模大赛)">
              <span class="honor-badge national">国家级</span>
              <span class="honor-name">全国大学生数学建模竞赛二等奖</span>
              <div class="honor-actions">
                <button class="detail-btn" @click.stop="openModal('全国大学生数学建模竞赛二等奖', 全国大学生建模大赛)">
                  <span class="btn-text">详情</span>
                </button>
                <span class="honor-year">2025</span>
              </div>
              <div class="hover-tooltip">点击查看详情</div>
            </li>
            <li class="honor-item" @click="openModal('蓝桥杯全国软件和信息技术专业人才大赛优秀奖', 蓝桥杯国优)">
              <span class="honor-badge national">国家级</span>
              <span class="honor-name">蓝桥杯全国软件和信息技术专业人才大赛优秀奖</span>
              <div class="honor-actions">
                <button class="detail-btn" @click.stop="openModal('蓝桥杯全国软件和信息技术专业人才大赛优秀奖', 蓝桥杯国优)">
                  <span class="btn-text">详情</span>
                </button>
                <span class="honor-year">2025</span>
              </div>
              <div class="hover-tooltip">点击查看详情</div>
            </li>
            <li class="honor-item" @click="openModal('国家励志奖学金', 优秀学生奖学金)">
              <span class="honor-badge national">国家级</span>
              <span class="honor-name">国家励志奖学金</span>
              <div class="honor-actions">
                <button class="detail-btn" @click.stop="openModal('国家励志奖学金', 优秀学生奖学金)">
                  <span class="btn-text">详情</span>
                </button>
                <span class="honor-year">2次</span>
              </div>
              <div class="hover-tooltip">点击查看详情</div>
            </li>
          </ul>
        </div>
        <div class="honor-category">
          <h4 class="honor-category-title">
            <span class="category-icon">🥇</span>
            省部级奖项
          </h4>
          <ul class="honor-list">
            <li class="honor-item" @click="openModal('服务外包大赛西南赛区三等奖', 服务外包大赛)">
              <span class="honor-badge provincial">省级</span>
              <span class="honor-name">服务外包大赛西南赛区三等奖</span>
              <div class="honor-actions">
                <button class="detail-btn" @click.stop="openModal('服务外包大赛西南赛区三等奖', 服务外包大赛)">
                  <span class="btn-text">详情</span>
                </button>
                <span class="honor-year">2025</span>
              </div>
              <div class="hover-tooltip">点击查看详情</div>
            </li>
            <li class="honor-item" @click="openModal('计算机设计大赛省三等奖', 计算机设计大赛)">
              <span class="honor-badge provincial">省级</span>
              <span class="honor-name">计算机设计大赛省三等奖</span>
              <div class="honor-actions">
                <button class="detail-btn" @click.stop="openModal('计算机设计大赛省三等奖', 计算机设计大赛)">
                  <span class="btn-text">详情</span>
                </button>
                <span class="honor-year">2025</span>
              </div>
              <div class="hover-tooltip">点击查看详情</div>
            </li>
            <li class="honor-item" @click="openModal('全国大学生市场调查与分析大赛省一等奖', 市调大赛证明)">
              <span class="honor-badge provincial">省级</span>
              <span class="honor-name">全国大学生市场调查与分析大赛省一等奖</span>
              <div class="honor-actions">
                <button class="detail-btn" @click.stop="openModal('全国大学生市场调查与分析大赛省一等奖', 市调大赛证明)">
                  <span class="btn-text">详情</span>
                </button>
                <span class="honor-year">2025</span>
              </div>
              <div class="hover-tooltip">点击查看详情</div>
            </li>
          </ul>
        </div>
        <div class="honor-category">
          <h4 class="honor-category-title">
            <span class="category-icon">🎓</span>
            校级荣誉
          </h4>
          <ul class="honor-list">
            <li class="honor-item" @click="openModal('优秀学生奖学金', 优秀学生奖学金)">
              <span class="honor-badge school">校级</span>
              <span class="honor-name">优秀学生奖学金（5次）</span>
              <div class="honor-actions">
                <button class="detail-btn" @click.stop="openModal('优秀学生奖学金', 优秀学生奖学金)">
                  <span class="btn-text">详情</span>
                </button>
                <span class="honor-year">2023-2026</span>
              </div>
              <div class="hover-tooltip">点击查看详情</div>
            </li>
            <li class="honor-item" @click="openModal('互联网+校级铜奖', 互联网铜奖)">
              <span class="honor-badge school">校级</span>
              <span class="honor-name">"互联网+"校级铜奖</span>
              <div class="honor-actions">
                <button class="detail-btn" @click.stop="openModal('互联网+校级铜奖', 互联网铜奖)">
                  <span class="btn-text">详情</span>
                </button>
                <span class="honor-year">2025</span>
              </div>
              <div class="hover-tooltip">点击查看详情</div>
            </li>
            <li class="honor-item" @click="openModal('开放实验校级立项', 校级项目立项)">
              <span class="honor-badge school">校级</span>
              <span class="honor-name">开放实验校级立项</span>
              <div class="honor-actions">
                <button class="detail-btn" @click.stop="openModal('开放实验校级立项', 校级项目立项)">
                  <span class="btn-text">详情</span>
                </button>
                <span class="honor-year">2025</span>
              </div>
              <div class="hover-tooltip">点击查看详情</div>
            </li>
          </ul>
        </div>
      </div>
    </div>

    <!-- 专业技能 -->
    <div class="content-section">
      <h3 class="section-title">专业技能</h3>
      <div class="skills-container">
        <div class="skill-group">
          <h4 class="skill-group-title">编程语言</h4>
          <div class="skill-tags">
            <span class="skill-tag">C</span>
            <span class="skill-tag">Java</span>
            <span class="skill-tag">Python</span>
            <span class="skill-tag">JavaScript</span>
            <span class="skill-tag">MySQL</span>
          </div>
        </div>
        <div class="skill-group">
          <h4 class="skill-group-title">框架与工具</h4>
          <div class="skill-tags">
            <span class="skill-tag">Spring Boot</span>
            <span class="skill-tag">Vue.js</span>
            <span class="skill-tag">LangChain</span>
            <span class="skill-tag">Ollama</span>
            <span class="skill-tag">Docker</span>
          </div>
        </div>
        <div class="skill-group">
          <h4 class="skill-group-title">AI/ML</h4>
          <div class="skill-tags">
            <span class="skill-tag">深度学习</span>
            <span class="skill-tag">计算机视觉</span>
            <span class="skill-tag">大模型部署</span>
            <span class="skill-tag">Agent开发</span>
          </div>
        </div>
        <div class="skill-group">
          <h4 class="skill-group-title">开发工具</h4>
          <div class="skill-tags">
            <span class="skill-tag">Git</span>
            <span class="skill-tag">VSCode</span>
            <span class="skill-tag">JetBrains</span>
            <span class="skill-tag">Linux</span>
          </div>
        </div>
        <div class="skill-group">
          <h4 class="skill-group-title">绘图工具</h4>
          <div class="skill-tags">
            <span class="skill-tag">Visio</span>
            <span class="skill-tag">PowerPoint</span>
            <span class="skill-tag">Draw.io</span>
          </div>
        </div>
      </div>
    </div>

    <!-- 证明材料弹窗 -->
    <CertificateModal
      v-model:visible="modalVisible"
      :title="modalTitle"
      :image-src="modalImageSrc"
    />
  </section>
</template>

<script setup>
import { ref } from 'vue'
import CertificateModal from '../portfolio/CertificateModal.vue'

// 导入证书图片
import 国家级大学生创新创业训练计划 from '../assets/国家级大学生创新创业训练计划.png'
import 全国大学生建模大赛 from '../assets/全国大学生建模大赛.jpg'
import 蓝桥杯国优 from '../assets/蓝桥杯国优.jpg'
import 优秀学生奖学金 from '../assets/优秀学生奖学金.jpg'
import 服务外包大赛 from '../assets/服务外包大赛.jpg'
import 计算机设计大赛 from '../assets/计算机设计大赛.jpg'
import 互联网铜奖 from '../assets/互联网+铜奖.png'
import 校级项目立项 from '../assets/校级项目立项.png'
import 市调大赛证明 from '../assets/市调大赛证明.png'

const modalVisible = ref(false)
const modalTitle = ref('')
const modalImageSrc = ref('')

const openModal = (title, imageSrc) => {
  modalTitle.value = title
  modalImageSrc.value = imageSrc
  modalVisible.value = true
}
</script>

<style scoped>
.honors-skill-section {
  display: flex;
  flex-direction: column;
  gap: var(--spacing-xl);
}

.content-section {
  background: var(--color-bg);
  border-left: 3px solid var(--color-primary);
  background: linear-gradient(to right, rgba(59, 130, 246, 0.03), transparent);
  border: 1px solid var(--color-border);
  border-radius: 8px;
  padding: var(--spacing-md);
  box-shadow: 0 1px 3px rgba(0, 0, 0, 0.06);
  transition: all var(--transition-fast);
}

.content-section:hover {
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.08);
  border-color: var(--color-primary);
  transform: translateY(-2px);
}

.section-title {
  font-size: 1.5rem;
  font-weight: 600;
  color: var(--color-text);
  margin-bottom: var(--spacing-md);
  padding-bottom: var(--spacing-xs);
  border-bottom: 2px solid var(--color-primary);
  display: inline-block;
}

.stat-item {
  text-align: center;
  padding: var(--spacing-sm);
}

.stat-number {
  display: block;
  font-size: 2rem;
  font-weight: 700;
  color: var(--color-primary);
  line-height: 1;
  margin-bottom: 4px;
}

.stat-label {
  font-size: 0.875rem;
  color: var(--color-text-secondary);
}

/* 荣誉奖项容器 */
.honors-container {
  display: flex;
  flex-direction: column;
  gap: var(--spacing-lg);
}

.honor-category {
  background: var(--color-bg);
  border-radius: 8px;
  padding: var(--spacing-md);
  border: 1px solid var(--color-border);
  transition: all var(--transition-fast);
}

.honor-category:hover {
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.08);
  border-color: var(--color-primary);
  transform: translateY(-2px);
}

.honor-category-title {
  font-size: 1rem;
  font-weight: 600;
  color: var(--color-text);
  margin-bottom: var(--spacing-sm);
  display: flex;
  align-items: center;
  gap: 8px;
}

.category-icon {
  font-size: 1.2rem;
}

.honor-list {
  list-style: none;
  display: flex;
  flex-direction: column;
  gap: 8px;
}

.honor-item {
  display: flex;
  align-items: center;
  gap: 12px;
  padding: 8px 12px;
  background: var(--color-bg);
  border-radius: 6px;
  transition: all var(--transition-fast);
  cursor: pointer;
  position: relative;
}

.honor-item:hover {
  transform: translateX(4px);
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.08);
  background: linear-gradient(to right, rgba(59, 130, 246, 0.05), transparent);
}

.honor-badge {
  display: inline-block;
  padding: 2px 8px;
  font-size: 0.7rem;
  font-weight: 600;
  border-radius: 4px;
  white-space: nowrap;
  flex-shrink: 0;
}

.honor-badge.national {
  background: var(--color-primary);
  color: white;
}

.honor-badge.provincial {
  background: #e3f2fd;
  color: #1976d2;
}

.honor-badge.school {
  background: #f5f5f5;
  color: #616161;
}

.honor-name {
  flex: 1;
  font-size: 0.9rem;
  color: var(--color-text);
}

.honor-actions {
  display: flex;
  align-items: center;
  gap: 8px;
  flex-shrink: 0;
}

/* 详情按钮 */
.detail-btn {
  display: inline-flex;
  align-items: center;
  padding: 0.25rem 0.625rem;
  font-size: 0.75rem;
  font-weight: 600;
  color: var(--color-primary);
  background: rgba(59, 130, 246, 0.1);
  border: none;
  border-radius: 4px;
  cursor: pointer;
  transition: all 0.2s ease;
  pointer-events: auto;
}

.detail-btn:hover {
  background: var(--color-primary);
  color: white;
  transform: scale(1.05);
}

.honor-year {
  font-size: 0.8rem;
  color: var(--color-text-muted);
  flex-shrink: 0;
}

/* 悬浮提示 - 样式与按钮一致，仅在非按钮区域显示 */
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

/* 仅在条目悬浮且按钮不悬浮时显示提示 */
.honor-item:hover .detail-btn:not(:hover) ~ .hover-tooltip,
.honor-item:hover .honor-actions:not(:hover) ~ .hover-tooltip {
  opacity: 1;
  visibility: visible;
  transform: translateX(-50%) translateY(-4px);
}

/* 技能容器 */
.skills-container {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: var(--spacing-md);
}

.skill-group {
  background: var(--color-bg);
  padding: var(--spacing-md);
  border-radius: 8px;
  border: 1px solid var(--color-border);
  transition: all var(--transition-fast);
}

.skill-group:hover {
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.08);
  border-color: var(--color-primary);
  transform: translateY(-2px);
}

.skill-group-title {
  font-size: 0.9rem;
  font-weight: 600;
  color: var(--color-text);
  margin-bottom: var(--spacing-sm);
}

.skill-tags {
  display: flex;
  flex-wrap: wrap;
  gap: 6px;
}

.skill-tag {
  display: inline-block;
  padding: 4px 10px;
  font-size: 0.8rem;
  background: var(--color-bg);
  color: var(--color-text-secondary);
  border-radius: 4px;
  border: 1px solid var(--color-border);
  transition: all var(--transition-fast);
}

.skill-tag:hover {
  background: var(--color-primary);
  color: white;
  border-color: var(--color-primary);
}

/* 响应式 */
@media (max-width: 768px) {
  .skills-container {
    grid-template-columns: 1fr;
  }

  .honor-item {
    flex-wrap: wrap;
  }

  .honor-name {
    width: 100%;
    margin-bottom: 4px;
  }

  .honor-actions {
    width: 100%;
    justify-content: flex-end;
  }

  .honor-year {
    text-align: right;
  }

  .detail-btn {
    padding: 0.2rem 0.5rem;
    font-size: 0.7rem;
  }

  .hover-tooltip {
    display: none;
  }
}
</style>
