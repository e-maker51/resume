<template>
  <section class="education-section" id="education">
    <div class="content-section">
      <h2 class="section-title">教育背景</h2>

      <div class="education-main">
        <div class="education-card main-card">
          <div class="education-header">
            <div class="school-info">
              <div class="school-badge">双一流</div>
              <h3 class="school-name">西南石油大学</h3>
              <span class="school-location">四川省成都市</span>
            </div>
            <span class="education-period">2023 - 至今</span>
          </div>
          <div class="education-body">
            <div class="degree-info">
              <p class="education-degree">计算机与软件学院 | 软件工程</p>
              <div class="gpa-section" @click="openModal('绩点和排名证明', 绩点和排名)">
                <button class="detail-btn" @click.stop="openModal('绩点和排名证明', 绩点和排名)">
                  <span class="btn-text">详情</span>
                </button>
                <div class="gpa-badge">
                  <span class="gpa-label">GPA</span>
                  <span class="gpa-value">4.16/5.0</span>
                </div>
                <div class="hover-tooltip">点击查看详情</div>
              </div>
            </div>
            <div class="rank-info">
              <span class="rank-label">专业排名</span>
              <span class="rank-value">7/158 (前 5%)</span>
            </div>
            <div class="courses-section">
              <span class="courses-label">主修课程</span>
              <div class="courses-tags">
                <span class="course-tag">概率统计(99)</span>
                <span class="course-tag">高等数学(98)</span>
                <span class="course-tag">计算机系统基础(98)</span>
                <span class="course-tag">程序设计基础(97)</span>
                <span class="course-tag">数据结构与算法(96)</span>
                <span class="course-tag">数据库原理(95)</span>
                <span class="course-tag">软件分析与设计(93)</span>
                <span class="course-tag">Python机器学习(93)</span>
                <span class="course-tag">操作系统(91)</span>
              </div>
            </div>
          </div>
        </div>
      </div>

      <div class="stats-bar">
        <div class="stat-item">
          <span class="stat-number">7+</span>
          <span class="stat-label">科研与项目</span>
        </div>
        <div class="stat-item">
          <span class="stat-number">5+</span>
          <span class="stat-label">竞赛奖项</span>
        </div>
        <div class="stat-item">
          <span class="stat-number">5%</span>
          <span class="stat-label">专业排名</span>
        </div>
        <div class="stat-item">
          <span class="stat-number">4.15</span>
          <span class="stat-label">GPA/5.0</span>
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
import 绩点和排名 from '../assets/绩点和排名.png'

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
.education-section {
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

.education-main {
  margin-bottom: var(--spacing-md);
}

.education-card {
  background-color: var(--color-bg);
  border: 1px solid var(--color-border);
  border-radius: 8px;
  padding: var(--spacing-md);
  transition: all var(--transition-fast);
}

.education-card:hover {
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.08);
  border-color: var(--color-primary);
  transform: translateY(-2px);
}

.education-header {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  margin-bottom: var(--spacing-sm);
  flex-wrap: wrap;
  gap: var(--spacing-xs);
}

.school-info {
  display: flex;
  flex-direction: column;
  gap: 4px;
}

.school-badge {
  display: inline-block;
  padding: 1.5px 8px;
  font-size: 1rem;
  font-weight: 600;
  color: white;
  background: linear-gradient(135deg, #667feac8 0%, #764ba2 100%);
  border-radius: 8px;
  width: fit-content;
}

.school-name {
  font-size: 1.25rem;
  font-weight: 700;
  color: var(--color-text);
}

.school-location {
  font-size: 0.85rem;
  color: var(--color-text-muted);
}

.education-period {
  font-size: 0.9rem;
  font-weight: 600;
  color: var(--color-primary);
  background-color: var(--color-bg);
  padding: 4px 12px;
  border-radius: 6px;
}

.education-body {
  display: flex;
  flex-direction: column;
  gap: var(--spacing-sm);
}

.degree-info {
  display: flex;
  justify-content: space-between;
  align-items: center;
  flex-wrap: wrap;
  gap: var(--spacing-xs);
}

.education-degree {
  font-size: 1rem;
  font-weight: 600;
  color: var(--color-text);
}

.gpa-section {
  display: flex;
  align-items: center;
  gap: 8px;
  cursor: pointer;
  position: relative;
  padding: 4px;
  border-radius: 6px;
  transition: all var(--transition-fast);
}

.gpa-section:hover {
  background: linear-gradient(to right, rgba(59, 130, 246, 0.05), transparent);
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

.gpa-badge {
  display: flex;
  align-items: center;
  gap: 4px;
  padding: 4px 10px;
  background-color:  #1f37a5;
  color: rgb(255, 255, 255);
  border-radius: 6px;
}

.gpa-label {
  font-size: 0.9 rem;
  opacity: 0.9;
  font-weight: 700;
}

.gpa-value {
  font-size: 0.9rem;
  font-weight: 700;
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

/* 仅在gpa-section悬浮且按钮不悬浮时显示提示 */
.gpa-section:hover .detail-btn:not(:hover) ~ .hover-tooltip {
  opacity: 1;
  visibility: visible;
  transform: translateX(-50%) translateY(-4px);
}

.rank-info {
  display: flex;
  align-items: center;
  gap: var(--spacing-xs);
  background-color: var(--color-bg);
  border-radius: 6px;
  width: fit-content;
}

.rank-label {
  font-size: 0.85rem;
  color: var(--color-text-secondary);
}

.rank-value {
  font-size: 0.9rem;
  font-weight: 600;
  color: var(--color-primary);
}

.courses-section {
  margin-top: var(--spacing-xs);
}

.courses-label {
  display: block;
  font-size: 0.85rem;
  font-weight: 600;
  color: var(--color-text);
  margin-bottom: var(--spacing-xs);
}

.courses-tags {
  display: flex;
  flex-wrap: wrap;
  gap: 6px;
}

.course-tag {
  display: inline-block;
  padding: 4px 10px;
  font-size: 0.8rem;
  background-color: var(--color-bg);
  color: var(--color-text-secondary);
  border-radius: 4px;
  border: 1px solid var(--color-border);
  transition: all var(--transition-fast);
}

.course-tag:hover {
  background-color: var(--color-primary);
  color: white;
  border-color: var(--color-primary);
}

/* 统计数据条 */
.stats-bar {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: var(--spacing-sm);
  background: var(--color-bg);
  border: 1px solid var(--color-border);
  border-radius: 8px;
  transition: all var(--transition-fast);
}

.stats-bar:hover {
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.08);
  border-color: var(--color-primary);
  transform: translateY(-2px);
}

.stat-item {
  text-align: center;
  padding: var(--spacing-xs);
}

.stat-number {
  display: block;
  font-size: 1.5rem;
  font-weight: 700;
  color: var(--color-primary);
  line-height: 1;
  margin-bottom: 4px;
}

.stat-label {
  font-size: 0.8rem;
  color: var(--color-text-secondary);
}

@media (max-width: 768px) {
  .stats-bar {
    grid-template-columns: repeat(2, 1fr);
  }

  .education-header {
    flex-direction: column;
  }

  .degree-info {
    flex-direction: column;
    align-items: flex-start;
  }

  .gpa-section {
    width: 100%;
    justify-content: flex-start;
  }

  .courses-tags {
    gap: 4px;
  }

  .course-tag {
    font-size: 0.75rem;
    padding: 3px 8px;
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
