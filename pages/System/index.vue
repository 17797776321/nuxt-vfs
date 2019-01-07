<template>
  <div class="system-page">
    <div class="banner_box">
      <img 
        :src="bannerImg" 
        alt="">
    </div>
    <div class="box">
      <div class="tit">系统开发</div>
      <div class="tit_eng">System</div>
      <div class="option_box clearfix">
        <div class="option float-left mr">
          <img 
            src="http://www.vfengs.com/home/dist/vfs-web/assets/images/system1.png" 
            alt="">
          <div class="tit">功能全面</div>
          <div class="tit_eng">COMPREHENSIVE FUNCTION</div>
          <div class="line_box">
            <div class="line colorED5A8E"/>
          </div>
        </div>
        <div class="option float-left mr">
          <img 
            src="http://www.vfengs.com/home/dist/vfs-web/assets/images/system2.png" 
            alt="">
          <div class="tit">扩展性强</div>
          <div class="tit_eng">STRONG &nbsp;&nbsp; EXTENSION</div>
          <div class="line_box">
            <div class="line color03A5E3"/>
          </div>
        </div>
        <div class="option float-left">
          <img 
            src="http://www.vfengs.com/home/dist/vfs-web/assets/images/system3.png" 
            alt="">
          <div class="tit">兼容性好</div>
          <div class="tit_eng">GOOD COMPATIBILITY</div>
          <div class="line_box">
            <div class="line color58CD63"/>
          </div>
        </div>
        <div class="option float-left mr">
          <img 
            src="http://www.vfengs.com/home/dist/vfs-web/assets/images/system4.png" 
            alt="">
          <div class="tit">易操作</div>
          <div class="tit_eng">EASY<br>
            OPERATION</div>
          <div class="line_box">
            <div class="line color58CD63"/>
          </div>
        </div>
        <div class="option float-left mr">
          <img 
            src="http://www.vfengs.com/home/dist/vfs-web/assets/images/system5.png" 
            alt="">
          <div class="tit">多种设备同时操作</div>
          <div class="tit_eng">MULTIOLE <br>
            DEVICES</div>
          <div class="line_box">
            <div class="line color58CD63"/>
          </div>
        </div>
        <div class="option float-left">
          <div 
            class="tit" 
            style="color:#92c3fd">系统平台搭建</div>
          <div class="tit_eng">行业解决方案<br>
            个性化定制开发</div>
          <div class="line_box">
            <div class="line colorffffff"/>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import BannerImg from '@/assets/images/banner3.png'
export default {
  data() {
    return {
      bannerImg: BannerImg
    }
  }
}
</script>
<style lang="less">
.system-page {
  background-color: #f4f4f4;
  .tit_eng {
    padding-bottom: 0 !important;
  }
  .colorED5A8E {
    background-color: #ed5a8e;
  }
  .color03A5E3 {
    background-color: #03a5e3;
  }
  .color58CD63 {
    background-color: #58cd63;
  }
  .colorF08026 {
    background-color: #f08026;
  }
  .color19BFE3 {
    background-color: #19bfe3;
  }
  .colorffffff {
    background-color: #ffffff;
  }
  .option_box {
    padding: 0 0.266667rem; // 0 20
    .mr {
      margin-right: 0.133333rem; // 10
    }
    .option {
      width: 3.013333rem; //226
      padding: 0 0.333333rem; // 0 25
      background-color: #ffffff;
      padding-top: 0.8rem; //60
      padding-bottom: 0.373333rem; //20
      position: relative;
      text-align: center;
      margin-top: 1.173333rem; //88
      img {
        display: block;
        width: 1.493333rem; //112
        position: absolute;
        left: 0.8rem; //60
        top: -0.746667rem; //-56
      }
      .tit {
        font-size: 0.293333rem; //22
        color: #333333;
        line-height: 0.533333rem; //40
      }
      .tit_eng {
        font-size: 0.24rem; //18
        color: #333333;
        line-height: 0.48rem; //36
        padding-top: 0.16rem; //12
      }
      .line_box {
        padding: 0.16rem 0;
        .line {
          width: 1.266667rem; //95
          height: 0.04rem; //3
          margin: 0 auto;
        }
      }
    }
  }
}
</style>
