<template>
  <Teleport to="body">
    <Transition name="modal">
      <div v-if="visible" class="modal-overlay" @click="handleOverlayClick">
        <div class="modal-container" @click.stop>
          <div class="modal-header">
            <h3 class="modal-title">{{ title }}</h3>
            <button class="modal-close" @click="close">
              <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
                <line x1="18" y1="6" x2="6" y2="18"></line>
                <line x1="6" y1="6" x2="18" y2="18"></line>
              </svg>
            </button>
          </div>
          <div class="modal-body">
            <div class="certificate-image-container">
              <img v-if="imageSrc" :src="imageSrc" :alt="title" class="certificate-image" />
              <div v-else class="certificate-placeholder">
                <span>暂无证明材料</span>
              </div>
            </div>
          </div>
        </div>
      </div>
    </Transition>
  </Teleport>
</template>

<script setup>
const props = defineProps({
  visible: {
    type: Boolean,
    default: false
  },
  title: {
    type: String,
    default: '证明材料'
  },
  imageSrc: {
    type: String,
    default: ''
  }
})

const emit = defineEmits(['update:visible', 'close'])

const close = () => {
  emit('update:visible', false)
  emit('close')
}

const handleOverlayClick = () => {
  close()
}
</script>

<style scoped>
.modal-overlay {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background-color: rgba(0, 0, 0, 0.6);
  display: flex;
  align-items: center;
  justify-content: center;
  z-index: 9999;
  padding: var(--spacing-md);
  backdrop-filter: blur(4px);
}

/* 弹窗容器 - 参考 AboutHeroSection.vue 的 content-section 样式 */
.modal-container {
  background: var(--color-bg);
  border-left: 3px solid var(--color-primary);
  background: linear-gradient(to right, rgba(59, 130, 246, 0.03), transparent);
  border: 1px solid var(--color-border);
  border-radius: 8px;
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.15);
  max-width: 90vw;
  max-height: 90vh;
  width: 800px;
  overflow: hidden;
  display: flex;
  flex-direction: column;
  transition: all var(--transition-fast);
}

.modal-container:hover {
  box-shadow: 0 8px 24px rgba(0, 0, 0, 0.2);
  border-color: var(--color-primary);
}

.modal-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: var(--spacing-md);
  border-bottom: 2px solid var(--color-primary);
  background: var(--color-bg);
}

.modal-title {
  font-size: 1.25rem;
  font-weight: 600;
  color: var(--color-text);
  margin: 0;
  padding-bottom: 0;
  border-bottom: none;
}

.modal-close {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 36px;
  height: 36px;
  border: none;
  background: rgba(59, 130, 246, 0.1);
  color: var(--color-primary);
  border-radius: 4px;
  cursor: pointer;
  transition: all 0.2s ease;
}

.modal-close:hover {
  background: var(--color-primary);
  color: white;
  transform: scale(1.05);
}

.modal-body {
  padding: var(--spacing-md);
  overflow: auto;
  flex: 1;
  display: flex;
  align-items: center;
  justify-content: center;
  background-color: var(--color-bg-secondary);
}

.certificate-image-container {
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
}

.certificate-image {
  max-width: 100%;
  max-height: 70vh;
  object-fit: contain;
  border-radius: 8px;
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.15);
  border: 1px solid var(--color-border);
}

.certificate-placeholder {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 100%;
  height: 300px;
  background-color: var(--color-bg);
  border: 2px dashed var(--color-border);
  border-radius: 8px;
  color: var(--color-text-muted);
  font-size: 1rem;
}

/* Modal transition animations */
.modal-enter-active,
.modal-leave-active {
  transition: opacity 0.3s ease;
}

.modal-enter-from,
.modal-leave-to {
  opacity: 0;
}

.modal-enter-active .modal-container,
.modal-leave-active .modal-container {
  transition: transform 0.3s ease, opacity 0.3s ease;
}

.modal-enter-from .modal-container,
.modal-leave-to .modal-container {
  transform: scale(0.9);
  opacity: 0;
}

@media (max-width: 768px) {
  .modal-container {
    width: 100%;
    max-height: 95vh;
  }

  .modal-title {
    font-size: 1.1rem;
  }

  .certificate-image {
    max-height: 60vh;
  }
}
</style>
