<script setup>
import { ref } from 'vue'
import HelloWorld from './components/HelloWorld.vue'

const count = ref(0)
</script>

<template>
  <div class="app">
    <header>
      <h1>Vue 3 + Vite 简易应用</h1>
      <p>一个简单可用的 Vue3 + Vite 程序示例</p>
    </header>
    
    <main>
      <HelloWorld />
      
      <div class="counter-section">
        <h2>计数器示例</h2>
        <button @click="count++" class="counter-btn">
          点击计数: {{ count }}
        </button>
        <p class="tip">点击按钮增加计数</p>
      </div>
    </main>
    
    <footer>
      <p>&copy; 2026 Vue 3 + Vite 应用</p>
    </footer>
  </div>
</template>

<style scoped>
.app {
  min-height: 100vh;
  display: flex;
  flex-direction: column;
}

header {
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  color: white;
  padding: 2rem;
  text-align: center;
  box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
}

header h1 {
  margin: 0 0 0.5rem 0;
  font-size: 2.5rem;
}

header p {
  margin: 0;
  font-size: 1.2rem;
  opacity: 0.9;
}

main {
  flex: 1;
  max-width: 1200px;
  margin: 0 auto;
  padding: 2rem;
  width: 100%;
}

.counter-section {
  background: white;
  border-radius: 12px;
  padding: 2rem;
  margin-top: 2rem;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  text-align: center;
}

.counter-section h2 {
  color: #667eea;
  margin-bottom: 1.5rem;
}

.counter-btn {
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  color: white;
  border: none;
  padding: 1rem 2rem;
  font-size: 1.2rem;
  border-radius: 8px;
  cursor: pointer;
  transition: transform 0.2s, box-shadow 0.2s;
  font-weight: 600;
}

.counter-btn:hover {
  transform: translateY(-2px);
  box-shadow: 0 6px 12px rgba(102, 126, 234, 0.4);
}

.counter-btn:active {
  transform: translateY(0);
}

.tip {
  margin-top: 1rem;
  color: #666;
  font-size: 0.9rem;
}

footer {
  background: #f5f5f5;
  text-align: center;
  padding: 1.5rem;
  color: #666;
  margin-top: auto;
}

@media (max-width: 768px) {
  header h1 {
    font-size: 2rem;
  }
  
  header p {
    font-size: 1rem;
  }
  
  main {
    padding: 1rem;
  }
}
</style>
