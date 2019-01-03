<template>
  <section class="container">
    <div class="banner_box">
      <img 
        :src="banner" 
        alt="">
    </div>
  </section>
</template>

<script>
import Banner from '@/assets/images/banner.png'
export default {
  components: {},
  data() {
    return {
      banner: Banner
    }
  }
}
</script>

<style lang="less">
.container {
  padding: 80px 0 0 0;
  .banner_box {
    width: 100%;
    img {
      display: block;
      width: 100%;
    }
  }
}
</style>
