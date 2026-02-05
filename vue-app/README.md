# Vue 3 + Vite 简易应用

这是一个简单可用的 Vue 3 + Vite 程序示例。

## 功能特性

- ⚡ **快速开发** - 使用 Vite 构建工具，提供极快的冷启动和热模块替换
- 🎯 **Vue 3 组合式 API** - 使用最新的 Vue 3 组合式 API 编写组件
- 🚀 **性能优异** - 优化的构建工具链，生产环境性能出色
- 💡 **易于使用** - 简洁的代码结构，容易上手和维护

## 项目结构

```
vue-app/
├── src/
│   ├── components/      # Vue 组件
│   │   └── HelloWorld.vue
│   ├── assets/          # 静态资源
│   ├── App.vue          # 根组件
│   ├── main.js          # 应用入口
│   └── style.css        # 全局样式
├── index.html           # HTML 模板
├── vite.config.js       # Vite 配置
└── package.json         # 项目依赖
```

## 安装依赖

```bash
cd vue-app
npm install
```

## 开发运行

```bash
npm run dev
```

应用将在 `http://localhost:3000` 启动

## 生产构建

```bash
npm run build
```

构建产物将输出到 `dist` 目录

## 预览生产构建

```bash
npm run preview
```

## 技术栈

- **Vue 3** - 渐进式 JavaScript 框架
- **Vite** - 下一代前端构建工具
- **ES Modules** - 使用原生 ES 模块

## 开始开发

1. 修改 `src/App.vue` 来改变应用的主要布局
2. 在 `src/components/` 目录下创建新组件
3. 在 `src/style.css` 中添加全局样式
4. 享受 Vite 的热更新带来的极速开发体验！

## 了解更多

- [Vue 3 文档](https://cn.vuejs.org/)
- [Vite 文档](https://cn.vitejs.dev/)
