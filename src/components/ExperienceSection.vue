<template>
  <section class="experience-section" id="experience">
    <div class="content-section">
      <h2 class="section-title">实践经历</h2>

      <div class="experience-list">
        <article class="experience-card">
          <div class="experience-header">
            <div class="experience-role">
              <h3 class="role-title">计算机学院青志协委员</h3>
              <span class="role-org">西南石油大学计算机学院</span>
            </div>
            <span class="experience-period">2023</span>
          </div>
          <div class="experience-content">
            <ul class="experience-details">
              <li>主动参与并组织 10 余场青年志愿服务活动，涵盖社区服务、校园公益等多个领域</li>
              <li>累计志愿时长超 60 小时</li>
              <li>协调志愿者团队，提升活动组织效率与服务质量</li>
            </ul>
          </div>
        </article>

        <article class="experience-card">
          <div class="experience-header">
            <div class="experience-role">
              <h3 class="role-title">三下乡 · 青年红色筑梦之旅</h3>
              <span class="role-org">暑期社会实践项目</span>
            </div>
            <span class="experience-period">2024</span>
          </div>
          <div class="experience-content">
            <ul class="experience-details">
              <li>积极参与国家非遗棕编文化调研、资料整理与数字化宣传</li>
              <li>助力非遗传承与乡村文化振兴</li>
              <li>所在团队入围社会实践活动校级重点团队</li>
            </ul>
          </div>
        </article>
      </div>
    </div>

    <div class="content-section">
      <h3 class="subsection-title">英语水平</h3>
      <div class="cert-grid">
        <div class="cert-item">
          <div class="cert-icon">🌐</div>
          <div class="cert-info">
            <span class="cert-name">CET-6</span>
            <span class="cert-desc">大学英语六级</span>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.experience-section {
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

.subsection-title {
  font-size: 1.125rem;
  font-weight: 600;
  color: var(--color-text);
  margin-bottom: var(--spacing-md);
}

.experience-list {
  display: flex;
  flex-direction: column;
  gap: var(--spacing-lg);
}

.experience-card {
  background-color: var(--color-bg);
  border: 1px solid var(--color-border);
  border-radius: 8px;
  padding: var(--spacing-md);
  transition: all var(--transition-fast);
}

.experience-card:hover {
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.08);
  border-color: var(--color-primary);
  transform: translateY(-2px);
}

.experience-header {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  margin-bottom: var(--spacing-md);
  flex-wrap: wrap;
  gap: var(--spacing-sm);
}

.experience-role {
  display: flex;
  flex-direction: column;
  gap: var(--spacing-xs);
}

.role-title {
  font-size: 1.2rem;
  font-weight: 600;
  color: var(--color-text);
}

.role-org {
  font-size: 0.9rem;
  color: var(--color-text-secondary);
}

.experience-period {
  font-size: 0.9rem;
  font-weight: 500;
  color: var(--color-primary);
  background-color: var(--color-bg);
  padding: 0.375rem 0.75rem;
  border-radius: 6px;
}

.experience-details {
  list-style: none;
  display: flex;
  flex-direction: column;
  gap: var(--spacing-xs);
}

.experience-details li {
  font-size: 0.95rem;
  color: var(--color-text-secondary);
  padding-left: 1.25rem;
  position: relative;
  line-height: 1.6;
}

.experience-details li::before {
  content: '•';
  position: absolute;
  left: 0;
  color: var(--color-primary);
  font-weight: bold;
}

.cert-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
  gap: var(--spacing-md);
}

.cert-item {
  display: flex;
  align-items: center;
  gap: var(--spacing-sm);
  padding: var(--spacing-md);
  background-color: var(--color-bg);
  border: 1px solid var(--color-border);
  border-radius: 8px;
  transition: all var(--transition-fast);
}

.cert-item:hover {
  border-color: var(--color-primary);
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.08);
  transform: translateY(-2px);
}

.cert-icon {
  font-size: 1.5rem;
}

.cert-info {
  display: flex;
  flex-direction: column;
}

.cert-name {
  font-size: 1rem;
  font-weight: 600;
  color: var(--color-text);
}

.cert-desc {
  font-size: 0.85rem;
  color: var(--color-text-muted);
}

@media (max-width: 768px) {
  .experience-header {
    flex-direction: column;
  }

  .cert-grid {
    grid-template-columns: 1fr;
  }
}
</style>
