<template>
  <div class="header-component">
    <b-navbar 
      fixed = "top"
      toggleable="md" 
      type="dark" 
      variant="danger">
      <b-navbar-toggle target="nav_collapse"/>
      <b-navbar-brand href="javascript:void(0);">
        <img 
          :src="logo" 
          alt="">
      </b-navbar-brand>
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
