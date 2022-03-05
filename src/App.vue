<template>
  <div id="app">
    <TodoHeader></TodoHeader>
    <TodoInput @addTodo="addTodo"></TodoInput>
    <TodoItem :todoItems="todoItems" @removeItem="removeItem"></TodoItem>
    <TodoFooter :todoItems="todoItems" @clearAll="clearAll"></TodoFooter>
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
  },
  data() {
    return {
      todoItems: []
    }
  },
  methods: {
    addTodo(text, isChecked) {
      let flag = true;
      this.todoItems.forEach(item => {
        if (item.text === text) {
          alert("该项已存在");
          flag = false;
        }
      });

      if (flag) {
        this.todoItems.unshift({
          "text": text,
          "isChecked": isChecked
        });
      }

      console.log(this.todoItems);
    },
    removeItem(index) {
      this.todoItems.splice(index, 1);
    },
    clearAll() {
      this.todoItems = [];
    }
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
  height: 540px;
}
</style>
