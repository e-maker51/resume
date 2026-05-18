<template>
  <section class="projects-section" id="projects">
    <div class="content-section">
      <h2 class="section-title">科研竞赛与项目</h2>

      <div class="projects-list">
        <article class="project-card featured">
          <div class="project-header">
            <div class="project-badge">国家级立项 · 第一负责人</div>
            <span class="project-period">2025.06 - 至今</span>
          </div>
          <h3 class="project-title">智驭视界—全天候车牌识别系统</h3>
          <p class="project-subtitle">大学生创新创业训练计划国家级立项</p>
          <div class="project-content">
            <div class="project-section">
              <h4 class="section-label">主要内容</h4>
              <p class="section-text">
                针对车牌识别受图像模糊、雾、雨退化影响等问题，应用多任务级联耦合三大图像复原模型，
                结合 HLPR3 构建双阶段架构，通过相应工程优化，搭配前后端分层架构，
                实现高效实时的车牌识别系统。
              </p>
            </div>
            <div class="project-section">
              <h4 class="section-label">负责工作</h4>
              <ul class="work-list">
                <li><p>系统<strong>全栈</strong>开发：构建端到端<strong> Tensor 流式 Pipeline</strong>，<strong>多任务级联耦合</strong>三大模型</p></li>
                <li><p>完成<strong>内存零拷贝、异步视频流处理、TensorRT加速推理</strong>等工程优化</p></li>
                <li><p>后端基于 Spring Boot 实现核心功能，前端用 Vue3 搭建移动端优先界面，支撑<strong>实时视频分析</strong></p></li>
                <li><p>构建基于 <strong>RAG</strong> 的 <strong>AI 运维助手</strong>，实现智能增强</p></li>
              </ul>
            </div>
            <div class="project-section"> 
              <h4 class="section-label">项目收获</h4>
              <p class="section-text">
                实现高效实时车牌识别系统，相应图像退化场景下识别准确率提升至96%以上，流式处理节省约10.8%耗时；TensorRT加速推理经100次测试，NAFNet性能提升25.5%，DehazeNet性能提升182.0%。并在准备专利申请及结项事宜
              </p>
            </div>
          </div>
          <div class="project-tech">
            <span class="tech-tag">PyTorch</span>
            <span class="tech-tag">Spring Boot</span>
            <span class="tech-tag">Vue.js</span>
            <span class="tech-tag">计算机视觉</span>
            <span class="tech-tag">图像复原</span>
            <span class="tech-tag">全栈</span>
            <span class="tech-tag">TensorRT</span>
          </div>
        </article>

        <article class="project-card featured">
          <div class="project-header">
            <div class="project-badge">算法核心成员</div>
            <span class="project-period">2025.10 - 2026.02</span>
          </div>
          <h3 class="project-title">果卜坡地质形变预测及成灾因子分析</h3>
          <p class="project-subtitle">地质监测与灾害预警研究项目</p>
          <div class="project-content">
            <div class="project-section">
              <h4 class="section-label">主要内容</h4>
              <p class="section-text">
                针对果卜坡形变监测难以捕捉时空连续性、海量 InSAR 数据难以有效利用的问题，
                采用时空双注意力集成 ConvLSTM、Encoder-Decoder 架构时空深度学习框架，
                处理 12 维特征数据，实现高精度地表形变预测与成灾因子分析。
              </p>
            </div>
            <div class="project-section">
              <h4 class="section-label">负责工作</h4>
              <ul class="work-list">
                <li><p><strong>算法核心</strong>研发：设计<strong>自学习空间因果门</strong>机制，创新<strong>网格化区域相关性卷积</strong>算法</p></li>
                <li><p>构建<strong>时空双注意力</strong>深度学习框架，处理<strong>12 维 InSAR 特征数据</strong>，完成模型训练与调参</p></li>
                <li><p>完成<strong>消融实验</strong>对比分析、<strong>成灾因子</strong>量化分析及可视化呈现</p></li>
              </ul>
            </div>
            <div class="project-section">
              <h4 class="section-label">项目收获</h4>
              <p class="section-text">
                本模型相比于基于LSTM的强基线模型，MAE降低7.8%、PESD下降8.8%、置信带收窄8.5%，精度稳定性全面领先；<br>
                论文《Spatiotemporal dual attention network for field scale prediction of three dimensional landslide deformation from InSAR time series》
                中科院一区 Engineering Geology [第三作者] 在投
              </p>
            </div>
          </div>
          <div class="project-tech">
            <span class="tech-tag">ConvLSTM</span>
            <span class="tech-tag">区域卷积</span>
            <span class="tech-tag">InSAR</span>
            <span class="tech-tag">时空预测</span>
            <span class="tech-tag">时间与空间注意力</span>
            <span class="tech-tag">自学习空间因果门</span>
          </div>
        </article>

        <article class="project-card featured">
          <div class="project-header">
            <div class="project-badge">校企合作项目</div>
            <span class="project-period">2025.12 - 2026.03</span>
          </div>
          <h3 class="project-title">国家管网油气知识图谱平台</h3>
          <p class="project-subtitle">国家管网与高校的油气合作项目</p>
          <div class="project-content">
            <div class="project-section">
              <h4 class="section-label">主要内容</h4>
              <p class="section-text">
                针对国际科研分析平台资源垄断、跨源数据整合不足，及国内平台在油气管道领域存在的"数据孤岛"、检索浅显、智能基础缺失等问题，
                本项目打破资源壁垒，实现多源数据自动化整合，构建领域知识图谱，提供精准智能化支撑。
              </p>
            </div>
            <div class="project-section">
              <h4 class="section-label">负责工作</h4>
              <ul class="work-list">
                <li><p><strong>后端架构</strong>设计：采用<strong>SpringCloud + Flask + LangChain</strong>异步微服务架构</p></li>
                <li><p>完成<strong>Ollama 大模型本地部署</strong>、<strong>Token 文本分割调优</strong>及 Linux 服务器运维</p></li>
                <li><p>实现<strong>PDF 文本智能提取</strong>、大模型推理解析及<strong>万方数据平台</strong>对接</p></li>
              </ul>
            </div>
            <div class="project-section">
              <h4 class="section-label">项目收获</h4>
              <p class="section-text">
                通过与国家管网校企合作，积累企业级开发协作经验，熟悉规范化开发流程，提升技术落地与协同对接能力，增强各技术栈的实战应用能力。
              </p>
            </div>
          </div>
          <div class="project-tech">
            <span class="tech-tag">SpringCloud</span>
            <span class="tech-tag">Flask</span>
            <span class="tech-tag">LangChain</span>
            <span class="tech-tag">Ollama</span>
            <span class="tech-tag">知识图谱</span>
            <span class="tech-tag">Linux</span>
          </div>
        </article>

        <article class="project-card featured">
          <div class="project-header">
            <div class="project-badge">基于知识图谱的RAG智能问答系统</div>
            <span class="project-period">2026.02 - 2026.04</span>
          </div>
          <h3 class="project-title">船舶维修领域智能问答系统（SFQA）</h3>
          <p class="project-subtitle">基于RAG技术的专业智能问答服务</p>
          <div class="project-content">
            <div class="project-section">
              <h4 class="section-label">主要内容</h4>
              <p class="section-text">
                基于知识图谱的RAG智能问答系统，采用Neo4j与RAG技术构建专业智能问答服务，采用混合检索、问题分类策略，解决通用大模型专业知识不足、幻觉问题，
                支持船舶维修多领域故障诊断，支持本地私有化部署，实现AI应用落地。
              </p>
            </div>
            <div class="project-section">
              <h4 class="section-label">负责工作</h4>
              <ul class="work-list">
                <li><p>设计实现<strong>RAG核心检索系统</strong>，融合<strong>向量检索</strong>（ChromaDB）与<strong>BM25关键词检索</strong>，结合元数据增强提升检索精度</p></li>
                <li><p>搭建<strong>多格式文档处理流水线</strong>，支持多类型文件解析、智能文本切分及元数据管理，构建专业自定义知识库，支持高度解耦</p></li>
                <li><p>设计<strong>LLM服务架构</strong>，实现多提供商无缝切换、流式响应及问题分类，优化RAG Prompt模板</p></li>
              </ul>
            </div>
            <div class="project-section">
              <h4 class="section-label">项目收获</h4>
              <p class="section-text">
                精通RAG全链路工程实现，掌握向量数据库、混合检索及LLM本地化部署，积累AI应用工程化业务落地经验。
              </p>
            </div>
          </div>
          <div class="project-tech">
            <span class="tech-tag">知识图谱</span>
            <span class="tech-tag">Neo4j</span>
            <span class="tech-tag">RAG</span>
            <span class="tech-tag">Flask</span>
            <span class="tech-tag">Vue 3</span>
            <span class="tech-tag">ChromaDB</span>
            <span class="tech-tag">Ollama</span>
            <span class="tech-tag">llama.cpp</span>
            <span class="tech-tag">MySQL</span>
            <span class="tech-tag">混合检索</span>
          </div>
        </article>

        <div class="more-projects-wrapper">
          <button class="more-btn" @click="showMoreProjects = !showMoreProjects">
            <img src="@/assets/更多.svg" alt="更多" class="more-icon" />
            <span>{{ showMoreProjects ? '收起' : '更多项目' }}</span>
          </button>
        </div>

        <transition name="expand">
          <div v-if="showMoreProjects" class="more-projects">
            <article class="project-card featured">
              <div class="project-header">
                <div class="project-badge">校级立项项目</div>
                <span class="project-period">2024.11 - 2025.05</span>
              </div>
              <h3 class="project-title">校园舆情论坛</h3>
              <p class="project-subtitle">校园舆情监测与管理系统</p>
              <div class="project-content">
                <div class="project-section">
                  <h4 class="section-label">主要内容</h4>
                  <p class="section-text">
                    针对校园舆情监测与管理需求，采用 Spring Boot + MyBatis + WebSocket + Redis 技术栈，
                    实现功能完善的舆情论坛系统。系统包含用户端（帖子发布、点赞、评论、举报）和管理端（舆情监控、数据统计、内容审核）。
                    核心亮点包括：舆情值算法实时计算帖子热度，WebSocket 实现消息实时推送，Redis 缓存提升查询性能，
                    JWT 实现无状态身份认证，AOP 切面编程实现日志记录和自动字段填充。
                  </p>
                </div>
                <div class="project-section">
                  <h4 class="section-label">负责工作</h4>
                  <ul class="work-list">
                    <li><p><strong>后端核心</strong>设计与开发：负责<strong>舆情管理</strong>（举报处理、热度计算、舆情统计）、<strong>帖子管理</strong>（CRUD、分页查询、缓存优化）</p></li>
                    <li><p>实现<strong>多级评论嵌套</strong>与递归查询、<strong>数据统计分析</strong>（用户/帖子/评论数据可视化）、<strong>WebSocket 实时通信</strong></p></li>
                    <li><p>参与数据库设计、RESTful API 开发、<strong>JWT 权限认证</strong>、全局异常处理、操作日志记录等基础架构搭建</p></li>
                  </ul>
                </div>
                <div class="project-section">
                  <h4 class="section-label">项目收获</h4>
                  <p class="section-text">
                    深入掌握 Spring Boot 企业级开发流程，熟练运用 MyBatis 进行复杂 SQL 查询，理解 Redis 缓存策略。
                    提升业务分析能力，积累全双工通信经验，培养代码规范意识，为 Java 后端开发奠定基础。
                  </p>
                </div>
              </div>
              <div class="project-tech">
                <span class="tech-tag">Spring Boot</span>
                <span class="tech-tag">MyBatis</span>
                <span class="tech-tag">WebSocket</span>
                <span class="tech-tag">Redis</span>
                <span class="tech-tag">JWT</span>
                <span class="tech-tag">AOP</span>
              </div>
            </article>

            <article class="project-card featured">
              <div class="project-header">
                <div class="project-badge">科研启航计划</div>
                <span class="project-period">2025.07 - 2025.12</span>
              </div>
              <h3 class="project-title">基于扩散模型的心电信号噪声量化与去噪系统</h3>
              <p class="project-subtitle">ECG 信号智能处理研究</p>
              <div class="project-content">
                <div class="project-section">
                  <h4 class="section-label">主要内容</h4>
                  <p class="section-text">
                    针对 ECG 信号去噪易盲目性的问题，采用"先量化后去噪"思路，
                    学习两个开源项目的论文及模型技术，利用扩散模型实现 ECG 噪声自动化量化，
                    再进行针对性去噪，避免盲目去噪，实现噪声量化与去噪的协同实现。
                  </p>
                </div>
                <div class="project-section">
                  <h4 class="section-label">负责工作</h4>
                  <ul class="work-list">
                    <li><p>学习开源项目论文原理与模型结构，<strong>复现噪声量化模型</strong>核心逻辑，掌握 <strong>Superlet 变换</strong>、<strong>潜在扩散模型</strong>应用</p></li>
                    <li><p>学习去噪模型实现方法，设计<strong>先量化、后去噪</strong>协同流程，验证流程合理性</p></li>
                    <li><p>整理学习笔记与相应模型的复现代码</p></li>
                  </ul>
                </div>
                <div class="project-section">
                  <h4 class="section-label">项目收获</h4>
                  <p class="section-text">
                    深入学习扩散模型、score-based 去噪模型在 ECG 信号处理中的应用，掌握相关论文核心原理与模型实现逻辑。
                    提升 PyTorch 框架使用、时频分析及模型复现能力，培养"先量化后去噪"的科学思维，为医学信号处理及AI相关学习奠定基础。
                  </p>
                </div>
              </div>
              <div class="project-tech">
                <span class="tech-tag">PyTorch</span>
                <span class="tech-tag">扩散模型</span>
                <span class="tech-tag">Score-based</span>
                <span class="tech-tag">Superlet 变换</span>
                <span class="tech-tag">ECG 信号处理</span>
                <span class="tech-tag">时频分析</span>
              </div>
            </article>
          </div>
        </transition>

        <div class="competitions-grid">
          <article class="competition-card">
            <div class="competition-badge">全国二等奖</div>
            <h4 class="competition-title">全国大学生数学建模竞赛</h4>
            <p class="competition-desc">
              运用<strong>PSO 算法</strong>和<strong>GA-SA 融合算法</strong>求解单无人机投放起爆参数，
              最大化导弹遮蔽时长及<strong>5 机 3 弹多目标优化</strong>问题。
            </p>
            <span class="competition-date">2025.09</span>
          </article>

          <article class="competition-card">
            <div class="competition-badge">西南赛区三等奖</div>
            <h4 class="competition-title">软件服务外包大赛</h4>
            <p class="competition-desc">
              <strong>后端主导开发</strong>：搭建系统框架，实现<strong>眼底图像分析</strong>、
              <strong>诊断报告生成</strong>、AI 问答等核心功能。
            </p>
            <span class="competition-date">2025.01 - 2025.03</span>
          </article>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref } from 'vue'

const showMoreProjects = ref(true)
</script>

<style scoped>
.projects-section {
  display: flex;
  flex-direction: column;
  gap: var(--spacing-lg);
}

.content-section {
  background: var(--color-bg);
  border: 1px solid var(--color-border);
  border-radius: 8px;
  padding: var(--spacing-md);
  box-shadow: 0 1px 3px rgba(0, 0, 0, 0.06);
}

.section-title {
  font-size: 1.4rem;
  font-weight: 600;
  color: var(--color-text);
  margin-bottom: var(--spacing-md);
  padding-bottom: var(--spacing-xs);
  border-bottom: 2px solid var(--color-primary);
  display: inline-block;
  letter-spacing: 0.5px;
}

.projects-list {
  display: flex;
  flex-direction: column;
  gap: var(--spacing-lg);
}

.project-card {
  background-color: var(--color-bg-secondary);
  border: 1px solid var(--color-border);
  border-radius: 8px;
  padding: var(--spacing-md);
  transition: all var(--transition-fast);
}

.project-card:hover {
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.08);
  border-color: var(--color-primary);
  transform: translateY(-2px);
}

.project-card.featured {
  border-left: 3px solid var(--color-primary);
  background: linear-gradient(to right, rgba(59, 130, 246, 0.03), transparent);
}

.project-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: var(--spacing-sm);
  flex-wrap: wrap;
  gap: var(--spacing-xs);
}

.project-badge {
  display: inline-block;
  padding: 0.25rem 0.75rem;
  font-size: 1.25rem;
  font-weight: 600;
  color: rgb(56, 118, 225);
  background: linear-gradient(135deg, var(--color-primary) 0%, var(--color-primary-dark) 100%);
  border-radius: 4px;
  text-transform: uppercase;
  letter-spacing: 0.5px;
}

.project-period {
  font-size: 1rem;
  color: var(--color-text-muted);
  color: rgb(56, 118, 225);
  font-weight: 500;
  font-family: 'Courier New', monospace;
}

.project-title {
  font-size: 1.3rem;
  font-weight: 700;
  color: var(--color-text);
  margin-bottom: 0.25rem;
  line-height: 1.3;
}

.project-subtitle {
  font-size: 0.9rem;
  color: var(--color-text-secondary);
  margin-bottom: var(--spacing-sm);
  font-style: italic;
}

.project-content {
  display: flex;
  flex-direction: column;
  gap: var(--spacing-sm);
  margin-bottom: var(--spacing-sm);
}

.project-section {
  padding: var(--spacing-xs);
  background-color: var(--color-bg);
  border-radius: 6px;
  border-left: 2px solid var(--color-border);
}

.section-label {
  font-size: 1rem;
  font-weight: 600;
  color: var(--color-text);
  margin-bottom: 0.55rem;
  text-transform: uppercase;
  letter-spacing: 0.5px;
}

.section-text {
  font-size: 0.9rem;
  color: var(--color-text-secondary);
  line-height: 1.9;
  text-align: justify;
}

.work-list {
  list-style: none;
  display: flex;
  flex-direction: column;
  gap: 0.25rem;
}

.work-list li {
  font-size: 0.9rem;
  color: var(--color-text-secondary);
  padding-left: 1rem;
  position: relative;
  line-height: 1.5;
  margin: 0;
}

.work-list li p {
  margin: 0;
  display: inline;
}

.work-list li::before {
  content: '▸';
  position: absolute;
  left: 0;
  color: var(--color-primary);
  font-weight: bold;
  font-size: 1rem;
  line-height: 1.5;
}

.project-tech {
  display: flex;
  flex-wrap: wrap;
  gap: 0.375rem;
  padding-top: var(--spacing-sm);
  border-top: 1px solid var(--color-border);
}

.tech-tag {
  display: inline-block;
  padding: 0.25rem 0.625rem;
  font-size: 0.8rem;
  background-color: var(--color-bg);
  color: var(--color-text-secondary);
  border-radius: 4px;
  border: 1px solid var(--color-border);
  transition: all var(--transition-fast);
  font-weight: 500;
}

.tech-tag:hover {
  background-color: var(--color-primary);
  color: white;
  border-color: var(--color-primary);
  transform: translateY(-1px);
}

.more-projects-wrapper {
  display: flex;
  justify-content: flex-start;
  margin: var(--spacing-sm) 0;
}

.more-btn {
  display: flex;
  align-items: center;
  gap: 0.5rem;
  padding: 0.6rem 1.2rem;
  background: linear-gradient(135deg, #3b82f6 0%, #1d4ed8 100%);
  color: white;
  border: 2px solid #2563eb;
  border-radius: 8px;
  font-size: 1rem;
  font-weight: 600;
  cursor: pointer;
  transition: all var(--transition-fast);
  box-shadow: 0 2px 8px rgba(59, 130, 246, 0.4);
}

.more-btn:hover {
  transform: translateY(-2px);
  box-shadow: 0 6px 20px rgba(59, 130, 246, 0.5);
  background: linear-gradient(135deg, #2563eb 0%, #1e40af 100%);
}

.more-icon {
  width: 1.2rem;
  height: 1.2rem;
  filter: brightness(0) invert(1);
}

.more-projects {
  display: flex;
  flex-direction: column;
  gap: var(--spacing-lg);
}

.expand-enter-active,
.expand-leave-active {
  transition: all 0.3s ease;
  max-height: 2000px;
  opacity: 1;
  overflow: hidden;
}

.expand-enter-from,
.expand-leave-to {
  max-height: 0;
  opacity: 0;
}

.competitions-grid {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: var(--spacing-md);
}

.competition-card {
  background-color: var(--color-bg);
  border-left: 3px solid var(--color-primary);
  background: linear-gradient(to right, rgba(59, 130, 246, 0.03), transparent);
  border: 1px solid var(--color-border);
  border-radius: 8px;
  padding: var(--spacing-md);
  transition: all var(--transition-fast);
  position: relative;
}

.competition-card:hover {
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.08);
  border-color: var(--color-primary);
  transform: translateY(-2px);
}

.competition-badge {
  display: inline-block;
  padding: 0.25rem 0.625rem;
  font-size: 0.75rem;
  font-weight: 600;
  color: white;
  background: linear-gradient(135deg, #c471edb2 0%, #f64f5ac4 100%);
  border-radius: 4px;
  margin-bottom: var(--spacing-xs);
  text-transform: uppercase;
  letter-spacing: 0.5px;
}

.competition-title {
  font-size: 1.05rem;
  font-weight: 600;
  color: var(--color-text);
  margin-bottom: var(--spacing-xs);
}

.competition-desc {
  font-size: 0.85rem;
  color: var(--color-text-secondary);
  line-height: 1.5;
  margin-bottom: var(--spacing-xs);
  text-align: justify;
}

.competition-date {
  font-size: 0.8rem;
  color: rgb(56, 118, 225);
  font-family: 'Courier New', monospace;
}

@media (max-width: 768px) {
  .project-header {
    flex-direction: column;
    align-items: flex-start;
  }

  .project-title {
    font-size: 1.15rem;
  }

  .competitions-grid {
    grid-template-columns: 1fr;
  }

  .tech-tag {
    font-size: 0.75rem;
  }

  .content-section {
    padding: var(--spacing-sm);
  }

  .project-card,
  .competition-card {
    padding: var(--spacing-sm);
  }
}
</style>
