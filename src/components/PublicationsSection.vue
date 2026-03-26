<template>
  <section class="section publications" id="publications">
    <div class="container">
      <h2 class="section-title">发表论文</h2>
      
      <div class="publications-list">
        <article 
          v-for="(pub, index) in publications" 
          :key="index"
          class="publication-card"
        >
          <div class="publication-content">
            <h3 class="publication-title">{{ pub.title }}</h3>
            <p class="publication-authors">
              <span 
                v-for="(author, aIndex) in pub.authors" 
                :key="aIndex"
                :class="{ 'author-highlight': author === '张明远' || author === 'Mingyuan Zhang' }"
              >
                {{ author }}<span v-if="aIndex < pub.authors.length - 1">, </span>
              </span>
            </p>
            <p class="publication-venue">
              <span class="venue-name">{{ pub.venue }}</span>
              <span v-if="pub.year" class="venue-year">{{ pub.year }}</span>
            </p>
            <div class="publication-tags">
              <span v-for="(tag, tIndex) in pub.tags" :key="tIndex" class="tag">{{ tag }}</span>
            </div>
            <div class="publication-links">
              <a v-if="pub.pdf" :href="pub.pdf" class="pub-link" target="_blank">
                <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" width="14" height="14">
                  <path d="M14 2H6a2 2 0 0 0-2 2v16a2 2 0 0 0 2 2h12a2 2 0 0 0 2-2V8z"></path>
                  <polyline points="14 2 14 8 20 8"></polyline>
                </svg>
                PDF
              </a>
              <a v-if="pub.code" :href="pub.code" class="pub-link" target="_blank">
                <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" width="14" height="14">
                  <polyline points="16 18 22 12 16 6"></polyline>
                  <polyline points="8 6 2 12 8 18"></polyline>
                </svg>
                Code
              </a>
              <a v-if="pub.project" :href="pub.project" class="pub-link" target="_blank">
                <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" width="14" height="14">
                  <path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path>
                  <path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path>
                </svg>
                Project
              </a>
            </div>
          </div>
        </article>
      </div>
      
      <div class="publications-more">
        <a href="#" class="btn btn-outline">
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" width="16" height="16">
            <line x1="8" y1="6" x2="21" y2="6"></line>
            <line x1="8" y1="12" x2="21" y2="12"></line>
            <line x1="8" y1="18" x2="21" y2="18"></line>
            <line x1="3" y1="6" x2="3.01" y2="6"></line>
            <line x1="3" y1="12" x2="3.01" y2="12"></line>
            <line x1="3" y1="18" x2="3.01" y2="18"></line>
          </svg>
          查看全部论文
        </a>
      </div>
    </div>
  </section>
</template>

<script setup>
const publications = [
  {
    title: "Vision-Language Pre-training with Contrastive Learning for Image-Text Understanding",
    authors: ["张明远", "李明", "王强", "张伟"],
    venue: "CVPR",
    year: "2024",
    tags: ["Vision-Language", "Contrastive Learning", "Pre-training"],
    pdf: "#",
    code: "#",
    project: "#"
  },
  {
    title: "Efficient Attention Mechanisms for High-Resolution Image Segmentation",
    authors: ["Chen Wang", "Mingyuan Zhang", "Jie Liu", "Hua Li"],
    venue: "ICCV",
    year: "2023",
    tags: ["Semantic Segmentation", "Attention", "Efficiency"],
    pdf: "#",
    code: "#",
    project: null
  },
  {
    title: "Multi-Scale Feature Fusion Network for Object Detection in Aerial Images",
    authors: ["张明远", "刘洋", "赵芳"],
    venue: "IEEE Transactions on Pattern Analysis and Machine Intelligence (TPAMI)",
    year: "2023",
    tags: ["Object Detection", "Aerial Images", "Feature Fusion"],
    pdf: "#",
    code: null,
    project: "#"
  },
  {
    title: "Self-Supervised Learning with Masked Autoencoders for Medical Image Analysis",
    authors: ["Yang Liu", "Mingyuan Zhang", "Wei Chen", "Xiaohong Wang"],
    venue: "NeurIPS",
    year: "2023",
    tags: ["Self-Supervised Learning", "Medical Imaging", "MAE"],
    pdf: "#",
    code: "#",
    project: null
  },
  {
    title: "Cross-Modal Retrieval with Adversarial Training",
    authors: ["张明远", "孙磊", "周杰"],
    venue: "ACM MM",
    year: "2022",
    tags: ["Cross-Modal Retrieval", "Adversarial Training", "Multimodal"],
    pdf: "#",
    code: "#",
    project: "#"
  },
  {
    title: "Knowledge Distillation for Lightweight Neural Networks",
    authors: ["Hao Li", "Mingyuan Zhang", "Qian Wang"],
    venue: "ECCV",
    year: "2022",
    tags: ["Knowledge Distillation", "Model Compression", "Lightweight"],
    pdf: "#",
    code: null,
    project: null
  }
]
</script>

<style scoped>
.publications {
  background-color: var(--color-bg-secondary);
}

.publications-list {
  display: flex;
  flex-direction: column;
  gap: var(--spacing-md);
}

.publication-card {
  background-color: var(--color-bg);
  border: 1px solid var(--color-border);
  border-radius: 8px;
  padding: var(--spacing-lg);
  transition: all var(--transition-normal);
}

.publication-card:hover {
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.08);
  border-color: var(--color-primary);
}

.publication-title {
  font-size: 1.1rem;
  font-weight: 600;
  color: var(--color-text);
  margin-bottom: var(--spacing-xs);
  line-height: 1.4;
}

.publication-authors {
  font-size: 0.9rem;
  color: var(--color-text-secondary);
  margin-bottom: var(--spacing-xs);
}

.author-highlight {
  color: var(--color-primary);
  font-weight: 500;
}

.publication-venue {
  font-size: 0.9rem;
  margin-bottom: var(--spacing-sm);
}

.venue-name {
  font-weight: 600;
  color: var(--color-text);
}

.venue-year {
  color: var(--color-text-muted);
  margin-left: var(--spacing-xs);
}

.publication-tags {
  display: flex;
  flex-wrap: wrap;
  gap: 0.5rem;
  margin-bottom: var(--spacing-sm);
}

.publication-links {
  display: flex;
  gap: var(--spacing-sm);
}

.pub-link {
  display: inline-flex;
  align-items: center;
  gap: 0.25rem;
  padding: 0.375rem 0.75rem;
  font-size: 0.8rem;
  font-weight: 500;
  color: var(--color-primary);
  background-color: var(--color-bg-secondary);
  border-radius: 4px;
  transition: all var(--transition-fast);
}

.pub-link:hover {
  background-color: var(--color-primary);
  color: white;
}

.publications-more {
  text-align: center;
  margin-top: var(--spacing-xl);
}

@media (max-width: 768px) {
  .publication-card {
    padding: var(--spacing-md);
  }
  
  .publication-title {
    font-size: 1rem;
  }
  
  .publication-links {
    flex-wrap: wrap;
  }
}
</style>
