<template>
  <div class="marketing-page">
    <div class="banner_box">
      <img 
        :src="bannerImg" 
        alt="">
    </div>
    <div class="box">
      <div class="tit">微信营销</div>
      <div class="tit_eng">Marketing</div>
      <div class="option_box clearfix">
        <div class="option float-left">
          <div class="content">
            <img 
              class="img" 
              src="http://www.vfengs.com/home/dist/vfs-web/assets/images/wechat1.png" 
              alt="">
            <div class="text">微商城</div>
          </div>
        </div>
        <div class="option float-left">
          <div class="content">
            <img 
              class="img" 
              src="http://www.vfengs.com/home/dist/vfs-web/assets/images/wechat2.png" 
              alt="">
            <div class="text">微官网</div>
          </div>
        </div>
        <div class="option float-left">
          <div class="content">
            <img 
              class="img" 
              src="http://www.vfengs.com/home/dist/vfs-web/assets/images/wechat3.png" 
              alt="">
            <div class="text">微活动</div>
          </div>
        </div>
      </div>
      <div class="banner">
        <img 
          :src="bannerimg2" 
          alt="">
      </div>
    </div>
  </div>
</template>
<script>
import BannerImg from '~/assets/images/banner3.png'
import Bannerimg2 from '~/assets/images/banner4.png'
export default {
  name: 'Marketing',
  data() {
    return {
      bannerImg: BannerImg,
      bannerimg2: Bannerimg2
    }
  }
}
</script>
<style lang="less">
.marketing-page {
  background-color: #f4f4f4;
  .option_box {
    padding: 0 0.266667rem; // 0 20
    .option {
      width: 33.3%;
      padding: 0 0.333333rem; // 0 25
      .content {
        background-color: #ffffff;
        padding: 0.293333rem 0; //22 0
        img {
          display: block;
          width: 1.666667rem; //125
          margin: 0 auto;
        }
        .text {
          padding-top: 0.32rem; //24
          font-size: 0.44rem; //33
          color: #333333;
          line-height: 0.826667rem; //62
        }
      }
    }
  }
  .banner {
    margin-top: 0.933333rem; //70
    width: 100%;
    img {
      display: block;
      width: 100%;
    }
  }
}
</style>
