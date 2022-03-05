<template>
  <footer>
    <div class="clear-wrap">
      <button class="clear-all" @click="clearAll">
        清除全部
      </button>
    </div>
    <p>&copy;2022 Powered by rylanwe</p>
  </footer>
</template>

<script>
export default {
  name: 'TodoFooter',
  methods: {
    clearAll() {
      this.$emit("clearAll");
    }
  }
}
</script>

<style scoped>
.clear-all {
  border: none;
  width: 100%;
  height: 40px;
  font-size: 16px;
  background-color: #08f;
  color: #fff;
}

p {
  border-top: 1px solid #eee;
  width: 100%;
  height: 25px;
  text-align: center;
  line-height: 25px;
  color: #bbb;
}
</style>