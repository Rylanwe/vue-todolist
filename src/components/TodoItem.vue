<template>
  <div class="wrap">
    <ul class="list">
      <li class="list-item">
        <input type="checkbox">
        <span>hello</span>
        <button class="btn">
          <i class="fas fa-trash"></i>
        </button>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'TodoItem'
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
  width: 100%;
  height: 40px;
  line-height: 40px;
  background-color: #dff0d8;
}

.list-item span {
  padding-left: 10px;
}

.list-item span.checked {
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