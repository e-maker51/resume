<template>
  <section class="about-section" id="about">
    <!-- 个人简介 -->
    <div class="content-section">
      <h2 class="section-title">简述</h2>
      <div class="bio-content">
        <ul class="describe-list">
            <li><strong>个人简述</strong>：专业排名<strong>5/158</strong>，位居年级前<strong>3.1%</strong>，<strong>GPA 4.15/5.0</strong>，概率统计、高等数学、数据结构、计算机系统基础等核心课程均取得<strong>95分以上</strong>优异成绩，
                具备扎实的数学功底与计算机理论基础。熟练掌握C、Java、Python、MySQL以及<strong>Agent开发</strong>、<strong>LangChain框架</strong>、<strong>Ollama大模型部署</strong>等AI技术栈，
                同时掌握<strong>Docker</strong>、<strong>Linux</strong>、<strong>Git</strong>等工程化工具，编程能力与系统开发能力兼备。在校期间，累计获得<strong>5次优秀学生奖学金</strong>、<strong>2次国家励志奖学金</strong>，斩获<strong>国家级、省部级</strong>学科竞赛与科研荣誉十余项，
                学业成绩、综合素养与科研潜力均得到充分检验。
            </li>
            <li><strong>核心研究方向</strong>：聚焦于<strong>大模型应用开发</strong>、<strong>时空深度学习</strong>、<strong>计算机视觉</strong>与<strong>智能系统构建</strong>，重点探索人工智能技术在<strong>能源地质</strong>、<strong>交通监控</strong>、<strong>工业数字化</strong>等实际工程场景的融合落地。
            </li>
            <li><strong>科研与项目实践</strong>：具备从<strong>算法创新</strong>到<strong>工程落地</strong>的全流程研发能力，在<strong>计算机视觉</strong>、<strong>时空深度学习</strong>与<strong>大模型应用</strong>三个方向形成了完整的技术积累与项目经验。
                <a href="#projects" class="project-nav-link" title="查看项目详情">
                    <img src="@/assets/详情.svg" alt="详情" class="nav-icon-img" width="16" height="16" />
                    <span class="nav-text">点击查看详情</span>
                </a>

                <strong><br>① 全天候车牌识别系统（国家级大创 · 第一负责人）</strong>：构建<strong>端到端 Tensor 流式 Pipeline</strong>，采用<strong>多任务级联耦合</strong>架构融合三大图像复原模型，
                实现<strong>雨雾模糊场景下的高精度车牌识别</strong>。完成<strong>内存零拷贝</strong>、<strong>异步视频流处理</strong>等工程优化，基于 <strong>Spring Boot + Vue3</strong> 构建前后端分离架构，支撑<strong>实时视频分析</strong>。
                项目已进入<strong>专利申请阶段</strong>。

                <strong><br>② 果卜坡地质形变预测（算法核心成员）</strong>：设计<strong>时空双注意力机制</strong>融合 <strong>ConvLSTM-Encoder-Decoder</strong> 框架，
                创新<strong>自学习空间因果门</strong>与<strong>网格化区域相关性卷积</strong>算法，实现<strong>12 维 InSAR 数据</strong>的高效处理与<strong>高精度三维滑坡形变预测</strong>。
                以<strong>第三作者</strong>身份撰写论文，已投稿至<strong>中科院一区</strong>《Engineering Geology》。

                <strong><br>③ 国家管网油气知识图谱平台（校企合作）</strong>：采用 <strong>SpringCloud + Flask + LangChain</strong> 构建<strong>异步微服务架构</strong>，
                完成 <strong>Ollama 大模型本地部署</strong>与<strong>Token 调优</strong>，实现<strong>PDF 智能提取</strong>、<strong>大模型推理解析</strong>及<strong>万方数据平台对接</strong>，
                探索大模型在<strong>知识图谱构建</strong>与<strong>智能问答</strong>场景的工业级应用。
            </li>
            <li><strong>学习与科研规划</strong>：第一，系统夯实<strong>大模型</strong>、<strong>时空深度学习</strong>、<strong>计算机视觉</strong>等领域的理论基础，紧跟学术前沿，提升学术研究深度；
                第二，积极参与导师课题组科研项目，将理论研究与各类实际场景深度结合，持续优化算法与技术方案，力争产出<strong>高质量学术论文</strong>与<strong>实用成果</strong>；
                第三，强化<strong>跨学科协作</strong>、<strong>学术写作</strong>与<strong>工程创新</strong>能力，补齐自身短板；
                第四，保持科研热忱与严谨态度，深耕<strong>人工智能与工程应用</strong>交叉领域，努力成长为兼具<strong>理论研究</strong>与<strong>工程实践能力</strong>的复合型人才，
                以技术创新解决实际问题，为行业智能化发展贡献力量。
            </li>
        </ul>
      </div>
    </div>

  </section>
</template>

<style scoped>
.describe-list {
  list-style: none;
  display: flex;
  flex-direction: column;
  gap: var(--spacing-md);
}

.describe-list li {
  font-size: 0.95rem;
  color: var(--color-text-secondary);
  padding-left: 1.5rem;
  position: relative;
  line-height: 1.7;
  text-align: justify;
}

.describe-list li::before {
  content: '';
  position: absolute;
  left: 0;
  top: 0.5em;
  width: 0;
  height: 0;
  border-left: 6px solid var(--color-primary);
  border-top: 4px solid transparent;
  border-bottom: 4px solid transparent;
}

.describe-list li:hover::before {
  border-left-color: var(--color-primary-light);
}

.about-section {
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

.project-nav-link {
  display: inline-flex;
  align-items: center;
  gap: 4px;
  margin-left: 8px;
  padding: 4px 8px;
  color: var(--color-primary);
  background: rgba(59, 130, 246, 0.1);
  border-radius: 4px;
  transition: all 0.2s ease;
  vertical-align: middle;
  text-decoration: none;
  font-size: 0.85rem;
}

.project-nav-link:hover {
  background: var(--color-primary);
  color: white;
  transform: scale(1.05);
}

.nav-icon-img {
  display: block;
  filter: none;
  transition: filter 0.2s ease;
}

.project-nav-link:hover .nav-icon-img {
  filter: brightness(0) invert(1);
}

.nav-text {
  font-size: 0.85rem;
}
</style>
