<template>
  <div class="header-component">
    <b-navbar
      toggleable="md" 
      type="dark" 
      variant="danger">
      <img
        :src="logo"
        class="logo"
        alt="">
      <b-navbar-toggle 
        target="nav_collapse" 
        v-html="''"/>
      <b-collapse 
        id="nav_collapse" 
        is-nav>
        <b-navbar-nav>
          <b-nav-item href="javascript:void(0);">首页</b-nav-item>
          <b-nav-item href="javascript:void(0);">联系我们</b-nav-item>
        </b-navbar-nav>
      </b-collapse>
    </b-navbar>
  </div>
</template>
<style lang="less">
.header-component {
  .logo {
    width: 190px;
  }
  .navbar-toggler {
    width: 52px;
    height: 52px;
    padding: 0;
    border: none;
    // background: url('../');
  }
}
</style>
<script>
import Logo from '@/assets/images/vfs_logo.png'
export default {
  name: 'Header',
  data() {
    return {
      logo: Logo
    }
  }
}
</script>
