<template>
  <div id="app">
    <h1>Vue Demo</h1>
    <HelloWorld msg="欢迎使用 Vue Demo" />
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: { HelloWorld }
}
</script>

<style>
#app { font-family: Avenir, Helvetica, Arial, sans-serif; padding: 2rem; }
</style>
