<template>
  <div class="hello">
    <h2>{{ msg }}</h2>
    <button @click="count++">点击次数: {{ count }}</button>
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
.hello { margin-top: 1rem; }
button { padding: 0.5rem 1rem; margin-top: 0.5rem; }
</style>
