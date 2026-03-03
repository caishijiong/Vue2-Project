<template>
  <div class="wrapper">
    <v-Header></v-Header>
    <div class="content-container">
      <v-SidebarItem></v-SidebarItem>
      <div class="main-content">
        <h1>这是一个主页组件</h1>
        <router-view></router-view>
      </div>
    </div>
  </div>
</template>

<script>
import vHeader from './Header.vue'
import vSidebarItem from './SidebarItem.vue'
export default {
  name: 'HomePage',
  components: {
    vSidebarItem,
    vHeader,
  },
}
</script>

<style scoped lang="scss">
.wrapper {
  display: flex;
  flex-direction: column;
}

.content-container {
  display: flex;
  flex: 1;
  overflow: hidden;
}

.main-content {
  flex: 1;
  padding: 20px;
}
</style>
