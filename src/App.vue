<template>
  <div id="app">
    <TodoHeader></TodoHeader>
    <TodoInput></TodoInput>
    <TodoItem></TodoItem>
    <TodoFooter></TodoFooter>
  </div>
</template>

<script>
import TodoHeader from './components/TodoHeader.vue'
import TodoInput from './components/TodoInput.vue'
import TodoItem from './components/TodoItem.vue'
import TodoFooter from './components/TodoFooter.vue'

export default {
  name: 'App',
  components: {
    TodoHeader,
    TodoInput,
    TodoItem,
    TodoFooter
  }
}
</script>

<style>
#app {
  overflow: hidden;
  margin: 50px auto;
  border: 1px solid #2f2f2f;
  border-radius: 20px;
  max-width: 450px;
  height: 500px;
}
</style>
