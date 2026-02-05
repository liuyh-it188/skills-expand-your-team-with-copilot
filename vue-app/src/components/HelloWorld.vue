<script setup>
import { ref } from 'vue'

const features = ref([
  { icon: '⚡', title: '快速开发', description: 'Vite 提供极快的冷启动和热更新' },
  { icon: '🎯', title: '组件化', description: 'Vue 3 组合式 API 让代码更加清晰' },
  { icon: '🚀', title: '性能优异', description: '优化的构建工具链，生产环境性能出色' },
  { icon: '💡', title: '易于使用', description: '简洁的语法，容易上手和维护' }
])

const showAlert = () => {
  alert('欢迎使用 Vue 3 + Vite！')
}
</script>

<template>
  <div class="hello">
    <h2>欢迎使用 Vue 3 + Vite</h2>
    <p class="intro">
      这是一个简单的 Vue 3 应用，使用 Vite 作为构建工具。
      下面是一些主要特性：
    </p>
    
    <div class="features">
      <div 
        v-for="(feature, index) in features" 
        :key="index" 
        class="feature-card"
      >
        <div class="icon">{{ feature.icon }}</div>
        <h3>{{ feature.title }}</h3>
        <p>{{ feature.description }}</p>
      </div>
    </div>
    
    <button @click="showAlert" class="action-btn">
      点击体验
    </button>
  </div>
</template>

<style scoped>
.hello {
  background: white;
  border-radius: 12px;
  padding: 2rem;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
}

h2 {
  color: #667eea;
  margin-bottom: 1rem;
  font-size: 2rem;
  text-align: center;
}

.intro {
  text-align: center;
  color: #666;
  line-height: 1.6;
  margin-bottom: 2rem;
  font-size: 1.1rem;
}

.features {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 1.5rem;
  margin-bottom: 2rem;
}

.feature-card {
  background: linear-gradient(135deg, #f5f7fa 0%, #c3cfe2 100%);
  padding: 1.5rem;
  border-radius: 10px;
  text-align: center;
  transition: transform 0.3s, box-shadow 0.3s;
}

.feature-card:hover {
  transform: translateY(-5px);
  box-shadow: 0 8px 15px rgba(0, 0, 0, 0.15);
}

.icon {
  font-size: 3rem;
  margin-bottom: 1rem;
}

.feature-card h3 {
  color: #333;
  margin-bottom: 0.5rem;
  font-size: 1.2rem;
}

.feature-card p {
  color: #666;
  line-height: 1.5;
  font-size: 0.95rem;
}

.action-btn {
  display: block;
  margin: 0 auto;
  background: #667eea;
  color: white;
  border: none;
  padding: 0.8rem 2rem;
  font-size: 1rem;
  border-radius: 8px;
  cursor: pointer;
  transition: background 0.3s, transform 0.2s;
  font-weight: 600;
}

.action-btn:hover {
  background: #5568d3;
  transform: scale(1.05);
}

.action-btn:active {
  transform: scale(1);
}

@media (max-width: 768px) {
  .features {
    grid-template-columns: 1fr;
  }
  
  h2 {
    font-size: 1.5rem;
  }
}
</style>
