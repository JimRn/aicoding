<template>
  <div id="app">
    <header class="site-header">
      <div class="container">
        <h1 class="logo">Vue Demo</h1>
        <p class="tagline">Vite + Vue 3 快速演示</p>
      </div>
    </header>

    <main class="container main-content">
      <section class="hero">
        <h2>快速上手</h2>
        <p>这是一个轻量级演示，包含组件示例与响应式样式。</p>
      </section>

      <section class="cards">
        <div class="card">
          <HelloWorld msg="欢迎使用 Vue Demo" />
        </div>
        <div class="card muted">
          <h3>说明</h3>
          <p>运行 <code>npm install</code> 后执行 <code>npm run dev</code> 查看效果。</p>
        </div>
      </section>
    </main>

    <footer class="site-footer">
      <div class="container">© 2026 Vue Demo</div>
    </footer>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: { HelloWorld }
}
</script>

<style scoped>
.container { max-width: 960px; margin: 0 auto; padding: 0 1rem; }
.site-header { background: linear-gradient(90deg,#4f46e5,#06b6d4); color: white; padding: 1.5rem 0; }
.logo { margin: 0; font-size: 1.5rem; }
.tagline { margin: 0.25rem 0 0; opacity: 0.95; }
.main-content { padding: 2rem 0; }
.hero { margin-bottom: 1.25rem; }
.hero h2 { margin: 0 0 0.5rem; }
.cards { display: grid; grid-template-columns: repeat(auto-fit,minmax(260px,1fr)); gap: 1rem; }
.card { background: white; border-radius: 8px; padding: 1rem; box-shadow: 0 6px 18px rgba(16,24,40,0.06); }
.card.muted { background: #f8fafc; color: #0f172a; }
.site-footer { text-align: center; padding: 1rem 0; color: #94a3b8; }

code { background: #0f172a0d; padding: 0.15rem 0.4rem; border-radius: 4px; font-family: ui-monospace, SFMono-Regular, Menlo, Monaco, "Roboto Mono", "Helvetica Neue", monospace; }
</style>
