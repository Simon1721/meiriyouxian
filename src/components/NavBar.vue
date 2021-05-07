<template>
    <div class="content-top">
        <!-- 菜单收起/展开按钮 -->
        <div class="menu-button">
          <a-button
            type="primary"
            @click="toggleCollapsed"
          >
            <a-icon :type="$store.state.collapsed ? 'menu-unfold' : 'menu-fold'" />
          </a-button>
        </div>
        <!-- 面包屑 -->
        <div class="crumbs">
          <a-breadcrumb>
            <a-breadcrumb-item>Home</a-breadcrumb-item>
            <a-breadcrumb-item
              ><a href="">Application Center</a></a-breadcrumb-item
            >
          </a-breadcrumb>
        </div>
        <!-- 用户信息 -->
        <div class="user-info">
          <ul>
            <li>Blue rain</li>
            <li>退出</li>
          </ul>
        </div>
      </div>
</template>

<script>
export default {
  methods: {
    toggleCollapsed() {
      this.$store.dispatch('toggleCollapsed');
    },
  },
};
</script>
