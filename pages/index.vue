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
          class="option_box"
          @click="jumpPage(item.href)">
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
    <!-- 案例 -->
    <div class="box">
      <div class="tit">案例</div>
      <div class="tit_eng">Case</div>
      <div class="case_box">
        <div 
          v-for="(item,index) in caseItem" 
          :key="index"
          class="img_box">
          <img 
            :src="item.img" 
            alt="">
        </div>
      </div>
    </div>
    <!-- 案例 -->
    <!-- 我们的品质 -->
    <div class="box">
      <div class="tit">我们的品质</div>
      <div class="tit_eng">Quality</div>
      <div class="quality_box clearfix">
        <div 
          v-for="(item,index) in qualityItems" 
          :key="index" 
          :class="{'mr20': (index+1) != qualityItems.length,'color92C3FD':index == 1}"
          class="option_box">
          <img 
            :src="item.img" 
            :alt="item.text" 
            class="img">
          <div class="text">{{ item.text }}</div>
          <div class="des">{{ item.des }}</div>
        </div>
      </div>
    </div>
    <!-- 我们的品质 -->
    <!-- 关于我们 -->
    <div class="box">
      <div class="tit">关于我们</div>
      <div class="tit_eng">About us</div>
      <div class="about_us_text">
        河南微风尚科技有限公司致力于互联网品牌建设与网络营销，专业领域包括网站建设、电子商务、移动互联网营销系统平台开发， 与其他网站建设及系统开发公司不同我们的整合解决方案结合了微风尚网络品牌建设经验和互联网整合营销的理念，并将策略和执行紧密结合，且不断评估并优化我们的方案，为客户提供一体化全方位的互联网品牌整合方案！
      </div>
    </div>
    <!-- 关于我们 -->
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

import Case1 from '@/assets/images/case1.png'
import Case2 from '@/assets/images/case2.png'
import Case3 from '@/assets/images/case3.png'

import Quality1 from '@/assets/images/quality1.png'
import Quality2 from '@/assets/images/quality2.png'
import Quality3 from '@/assets/images/quality3.png'
export default {
  components: {},
  data() {
    return {
      banner: Banner,
      items: [
        {
          img: Service1,
          text: '电商平台',
          ishad: false,
          href: 'Electronics'
        },
        {
          img: Service2,
          text: '微信营销',
          ishad: true,
          href: 'Marketing'
        },
        {
          img: Service3,
          text: 'App定制',
          ishad: true,
          href: 'Customization'
        },
        {
          img: Service4,
          text: '系统开发',
          ishad: false,
          href: 'System'
        },
        {
          img: Service5,
          text: '网站建设',
          ishad: false,
          href: 'Website'
        },
        {
          img: Service6,
          text: '客户案例',
          ishad: true
        }
      ],
      caseItem: [
        {
          img: Case1
        },
        {
          img: Case2
        },
        {
          img: Case3
        }
      ],
      qualityItems: [
        {
          img: Quality1,
          text: '技术领先',
          des: '始终走在行业的前端'
        },
        {
          img: Quality2,
          text: '服务领先',
          des: '始终已客户为主导'
        },
        {
          img: Quality3,
          text: '售后领先',
          des: '始终为您保驾护航'
        }
      ]
    }
  },
  methods: {
    jumpPage(path) {
      this.$router.push({ path: `/${path}` })
    }
  }
}
</script>

<style lang="less">
.container {
  padding: 0;
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
  .img_box {
    padding: 0 25px 25px 25px;
    img {
      display: block;
      width: 100%;
    }
  }
  .quality_box {
    .mr20 {
      margin-right: 25px;
    }
    .color92C3FD {
      background-color: #92c3fd;
      color: #ffffff;
      .text {
        color: #ffffff !important;
      }
      .des {
        color: #ffffff !important;
      }
    }
    .option_box {
      display: inline-block;
      width: 216px;
      height: 234px;
      box-shadow: 0 0 60px rgba(0, 0, 0, 0.15);
      .img {
        display: block;
        margin: 42px auto 0;
      }
      .text {
        font-size: 18px;
        color: #92c3fd;
        margin-top: 46px;
      }
      .des {
        font-size: 14px;
        color: #92c3fd;
        margin-top: 10px;
      }
    }
  }
  .about_us_text {
    font-size: 28px;
    color: #222222;
    padding: 0 25px;
  }
}
</style>
