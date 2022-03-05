<template>
  <div class="wrap">
    <ul class="list">
      <li
        class="list-item"
        v-for="(item, index) in todoItems"
        :key="item.text"
      >
        <input type="checkbox" @click="checked(item)">
        <span :class="{checked: item.isChecked}">{{ item.text }}</span>
        <button class="btn" @click="removeItem(index)">
          <i class="fas fa-trash"></i>
        </button>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'TodoItem',
  props: {
    todoItems: Array
  },
  methods: {
    checked(item) {
      item.isChecked = !item.isChecked;
    },
    removeItem(index) {
      this.$emit("removeItem", index);
    }
  }
}
</script>

<style scoped>
.wrap {
  overflow: auto;
  width: 100%;
  height: 390px;
}

.list .list-item {
  position: relative;
  padding-left: 10px;
  border-bottom: 1px solid #ddd;
  width: 100%;
  height: 40px;
  line-height: 40px;
}

.list-item span {
  padding-left: 10px;
}

.list-item span.checked {
  color: #888;
  text-decoration: line-through;
}

input[type="checkbox"] {
  transform: scale(1.5);
}

.list-item .btn {
  position: absolute;
  right: 0;
  padding: 0;
  border: none;
  width: 50px;
  height: 100%;
  background-color: transparent;
}





</style>