<template>
  <div class="wrap">
    <div class="input-bd">
      <input type="text" class="input" placeholder="请输入待办项">
    </div>
    <div class="btn-bd">
      <button class="btn">添加项目</button>
    </div>
  </div>
</template>

<script>
export default {
  name: 'TodoInput'
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