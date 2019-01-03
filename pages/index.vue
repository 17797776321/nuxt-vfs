<template>
  <section class="container">
    <div class="banner_box">
      <img 
        :src="banner" 
        alt="">
      <div class="tit">一站式服务  助力企业转型</div>
      <div class="des">十大行业解决方案  数百款营销活动 公众号</div>
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
    position: relative;
    img {
      display: block;
      width: 100%;
    }
    .tit {
      width: 100%;
      font-size: 40px;
      color: #ffffff;
      text-align: center;
      line-height: 60px;
      position: absolute;
      top: 222px;
    }
    .des {
      width: 100%;
      font-size: 16px;
      color: #ffffff;
      text-align: center;
      line-height: 48px;
      position: absolute;
      top: 278px;
    }
  }
}
</style>
