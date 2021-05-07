<template>
  <div class="home">
    <left-menu />
    <div :class="{ content: true, 'menu-unfold': $store.state.collapsed }">
      <nav-bar />
      <router-view></router-view>
    </div>
  </div>
</template>

<script>
import LeftMenu from '../components/Menu.vue';
import NavBar from '../components/NavBar.vue';

export default {
  data() {
    return {
    };
  },
  components: {
    LeftMenu,
    NavBar,
  },
  methods: {
  },
};
</script>
<style lang="less">
@import url("~@/assets/css/home.less");
</style>
