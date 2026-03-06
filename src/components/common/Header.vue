<template>
  <div class="header">
    <div class="header-content">
      <div class="collapse-btn" @click="collapseChange">
        <i v-if="folded" class="el-icon-s-fold"></i>
        <i v-else class="el-icon-s-unfold"></i>
      </div>
      <h1>这是一个头部组件</h1>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HeaderPage',
  props: {
    folded: Boolean,
  },
  data() {
    return {
      // folded: false,
    }
  },
  methods: {
    collapseChange() {
      this.$emit('collapse-change')
    },
  },
}
</script>

<style scoped lang="scss">
.header {
  display: flex;
  align-items: center;
  justify-content: space-between;
  background-color: #f5f5f5;
  height: 60px;
  flex-shrink: 0; /* 防止头部被压缩 */
}

.header-content {
  display: flex;
  align-items: center;
  
  .collapse-btn {
    width: 24px;
    cursor: pointer;
    align-items: center;
    padding: 0 14px;
    font-size: 20px;
  }
}
</style>