<template>
  <section class="container">
    <div class="banner_box">
      <img 
        :src="banner" 
        alt="">
      <div class="tit">一站式服务  助力企业转型</div>
      <div class="des">十大行业解决方案  数百款营销活动 公众号</div>
    </div>
    <div class="box">
      <div class="tit">服务项目</div>
      <div class="tit_eng">Service Items</div>
      <div class="options clearfix">
        <div 
          v-for="(item,index) in items" 
          :key="index" 
          :class="{'float-left':(index+1)%2 == 1,'float-right':(index+1)%2 == 0,'colorEFF0F0':item.ishad,'colorFBFBFB':!item.had}"
          class="option_box">
          <img
            :src="item.img"
            :alt="item.text" 
            class="option_img">
          <div class="option_text">
            {{ item.text }}
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import Banner from '@/assets/images/banner.png'
import Service1 from '@/assets/images/service1.png'
import Service2 from '@/assets/images/service2.png'
import Service3 from '@/assets/images/service3.png'
import Service4 from '@/assets/images/service4.png'
import Service5 from '@/assets/images/service5.png'
import Service6 from '@/assets/images/service6.png'
export default {
  components: {},
  data() {
    return {
      banner: Banner,
      items: [
        {
          img: Service1,
          text: '电商平台',
          ishad: false
        },
        {
          img: Service2,
          text: '微信营销',
          ishad: true
        },
        {
          img: Service3,
          text: 'App定制',
          ishad: true
        },
        {
          img: Service4,
          text: '系统开发',
          ishad: false
        },
        {
          img: Service5,
          text: '网站建设',
          ishad: false
        },
        {
          img: Service6,
          text: '客户案例',
          ishad: true
        }
      ]
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
  .options {
    padding: 0 25px;
    .colorFBFBFB {
      background-color: #fbfbfb;
    }
    .colorEFF0F0 {
      background-color: #eff0f0;
    }
    .option_box {
      width: 50%;
      padding: 80px 0 72px 0;
      .option_img {
        display: block;
        width: 154px;
        margin: 0 auto;
      }
      .option_text {
        font-size: 32px;
        color: #333333;
        line-height: 60px;
      }
    }
  }
}
</style>
