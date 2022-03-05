<template>
  <div id="app">
    <TodoHeader></TodoHeader>
    <main>
      <TodoInput></TodoInput>
      <TodoItem></TodoItem>
    </main>
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

</style>
