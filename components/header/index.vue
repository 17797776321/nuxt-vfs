<template>
  <div class="header-component">
    <b-navbar
      toggleable="md" 
      fixed="top">
      <img
        :src="logo"
        class="logo"
        alt="">
      <b-navbar-toggle 
        target="nav_collapse" 
        v-html="''"/>
      <b-collapse 
        id="nav_collapse" 
        is-nav 
        right>
        <b-navbar-nav>
          <b-nav-item href="javascript:void(0);">首页</b-nav-item>
          <b-nav-item href="javascript:void(0);">服务项目</b-nav-item>
          <b-nav-item href="javascript:void(0);">案例</b-nav-item>
          <b-nav-item href="javascript:void(0);">我们的品质</b-nav-item>
          <b-nav-item href="javascript:void(0);">关于我们</b-nav-item>
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
  .navbar {
    padding: 15px 25px;
    background-color: #ffffff !important;
    border-bottom: 1px solid #cccccc;
  }
  .navbar-toggler {
    width: 52px;
    height: 52px;
    padding: 0;
    border: none;
    background: url('../../assets/images/menu.png') no-repeat;
    background-size: 47px 35px;
    background-position: center center;
  }
  .nav-link {
    padding: 15px 0;
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
  },
  mounted() {
    console.log(this.$router)
  }
}
</script>
