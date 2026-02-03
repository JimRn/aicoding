<template>
  <div class="hello-card">
    <div class="hello-header">
      <h2>{{ msg }}</h2>
      <p class="subtitle">交互示例组件</p>
    </div>

    <div class="hello-body">
      <button class="btn-primary" @click="count++">
        点击次数： <span class="badge">{{ count }}</span>
      </button>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: { type: String, default: '' }
  },
  data() {
    return { count: 0 }
  }
}
</script>

<style scoped>
.hello-card { display: flex; flex-direction: column; gap: 0.75rem; }
.hello-header h2 { margin: 0; font-size: 1.125rem; }
.subtitle { margin: 0.25rem 0 0; color: #64748b; font-size: 0.9rem; }
.hello-body { display: flex; align-items: center; }
.btn-primary { background: linear-gradient(90deg,#4f46e5,#06b6d4); color: white; border: none; padding: 0.6rem 0.9rem; border-radius: 6px; cursor: pointer; display: inline-flex; align-items: center; gap: 0.6rem; font-weight: 600; }
.btn-primary:hover { transform: translateY(-1px); box-shadow: 0 6px 18px rgba(3,7,18,0.08); }
.badge { background: rgba(255,255,255,0.18); padding: 0.15rem 0.5rem; border-radius: 999px; }
</style>
