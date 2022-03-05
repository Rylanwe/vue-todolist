<template>
  <div class="wrap">
    <div class="input-bd">
      <input
        type="text"
        class="input"
        v-model="text"
        @keyup.enter="addTodo"
        placeholder="请输入待办项"
      />
    </div>
    <div class="btn-bd">
      <button class="btn" @click="addTodo">添加项目</button>
    </div>
  </div>
</template>

<script>
export default {
  name: 'TodoInput',
  data() {
    return {
      text: "",
      isChecked: false
    }
  },
  methods: {
    addTodo() {
      if (this.text !== "") {
        this.$emit("addTodo", this.text.trim(), this.isChecked);
        this.clearInput();
      }
    },
    clearInput() {
      this.text = "";
    }
  }
}
</script>

<style scoped>
.wrap {
  display: flex;
  width: 100%;
  height: 35px;
}

.input-bd {
  display: block;
  flex: 4;
  width: 80%;
  height: 100%;
}

.btn-bd {
  flex: 1;
  width: 100%;
  height: 100%;
}

.input {
  margin: 0;
  padding-left: 10px;
  border: 1px solid #2f2f2f;
  width: 100%;
  height: 100%;
  font-size: 18px;
}

.btn {
  border: none;
  height: 100%;
  width: 100%;
  font-size: 16px;
  background-color: #08f;
  color: #fff;
  cursor: pointer;
}
</style>