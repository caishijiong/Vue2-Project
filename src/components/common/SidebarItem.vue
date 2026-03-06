<template>
  <!-- <div v-if="!item.hidden"> -->
  <div class="sidebar" :class="{ 'sidebar-folded': folded }">
    1
    <!-- <template v-if="hasOneShowingChild(item.children,item) && (!onlyOneChild.children||onlyOneChild.noShowingChildren)&&!item.alwaysShow">
      <app-link v-if="onlyOneChild.meta" :to="resolvePath(onlyOneChild.path)">
        <el-menu-item :index="resolvePath(onlyOneChild.path)" :class="{'submenu-title-noDropdown':!isNest}">
          <item :icon="onlyOneChild.meta.icon||(item.meta&&item.meta.icon)" :title="onlyOneChild.meta.title" />
        </el-menu-item>
      </app-link>
    </template>

    <el-submenu v-else ref="subMenu" :index="resolvePath(item.path)" popper-append-to-body>
      <template slot="title">
        <item v-if="item.meta" :icon="item.meta && item.meta.icon" :title="item.meta.title" />
      </template>
      <sidebar-item
        v-for="child in item.children"
        :key="child.path"
        :is-nest="true"
        :item="child"
        :base-path="resolvePath(child.path)"
        class="nest-menu"
      />
    </el-submenu> -->
  </div>
</template>

<script>
export default {
  props: {
    folded: {
      type: Boolean,
      default: false,
    },
  },
}
</script>

<style scoped lang="scss">
.sidebar {
  height: 100vh;
  background-color: #f0f0f0;
  transition: width 0.3s ease; /* 添加平滑过渡效果 */
  display: flex;
  align-items: center;
  justify-content: center;
  overflow: hidden; 

  &.sidebar-folded {
    width: 64px; /* 折叠时的宽度 */
  }

  &:not(.sidebar-folded) {
    width: 200px; /* 展开时的宽度 */
  }
}
</style>
