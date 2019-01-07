<template>
  <div class="electronics-page">
    <div class="banner_box">
      <img 
        :src="bannerImg" 
        alt="">
    </div>
    <div class="box">
      <div class="tit">电子商务</div>
      <div class="tit_eng">Electronics</div>
      <div 
        v-for=" (item,index) in electronics"
        :key="index" 
        :class="{'bgcolorF4F4F4': (index+1)%2 == 1}"
        class="mybox clearfix" 
      >
        <div 
          :class="{'float-left': (index+1)%2 == 0,'float-right':((index+1)%2 == 1)}" 
          class="img_box">
          <img 
            :src="item.introImg" 
            alt="">
        </div>
        <div 
          :class="{'float-left': (index+1)%2 == 1,'float-right':(index+1)%2 == 0,'paddingLeft':(index+1)%2 == 0,'paddingRight':(index+1)%2 == 1}" 
          class="text_box">
          <h3 class="tit">{{ item.title }}</h3>
          <p class="cont">{{ item.content }}</p>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import BannerImg from '@/assets/images/banner3.png'
import Ds1 from '@/assets/images/ds1.png'
import Ds2 from '@/assets/images/ds2.png'
import Ds3 from '@/assets/images/ds3.png'
import Ds4 from '@/assets/images/ds4.png'
import Ds5 from '@/assets/images/ds5.png'
import Ds6 from '@/assets/images/ds6.png'
import Ds7 from '@/assets/images/ds7.png'
import Ds8 from '@/assets/images/ds8.png'
import Ds9 from '@/assets/images/ds9.png'
export default {
  name: 'Electronics',
  data() {
    return {
      bannerImg: BannerImg,
      electronics: [
        {
          introImg: Ds1,
          title: '用户体验设计',
          content:
            '微风尚强大的设计实力支撑，帮助客户跳出千篇一律的传统商城模板式网站，提升超强用户体验的感官设计，更加有利于产品及品牌展示，从而提升消费者的整个购物体验！'
        },
        {
          introImg: Ds2,
          title: '丰富的商品介绍',
          content:
            '促销价格、促销形式、商品评分、服务标签、商品属性、图片选择，您完全可以自定义商品购买页面的介绍内容，消费者更了解您的商品，就更愿意购买。'
        },
        {
          introImg: Ds3,
          title: 'SEO优化',
          content:
            '想要提升商城在搜索引擎的排名，让客户主动上门？没问题！商城内置标题描述关键词修改、网站地图、友链交换等多项SEO功能，助您快速提升关键词排名！'
        },
        {
          introImg: Ds4,
          title: '促销管理',
          content:
            '想要快速销售特定商品，却担心没有适用的促销功能？别担心！商城内置多种促销功能，直降、满减、团购、组合购买，让您轻松开展各种促销活动！'
        },
        {
          introImg: Ds5,
          title: '在线支付',
          content:
            '商城收款离不开网上银行的在线支付功能，商城内置所有银行的支付方式（包括支付宝、易宝等），您只需在我们的协助下进行简单的配置，就可以在线收款了'
        },
        {
          introImg: Ds6,
          title: '会员管理',
          content:
            '发展并积累真正属于您自己商城的忠实会员，掌握会员的手机号、邮件、地址等详细信息，并针对特定的会员群体做精准的短信和邮件营销'
        },
        {
          introImg: Ds7,
          title: '报表统计',
          content:
            '数据分析是一个网上商城成功的基石，商城内置了访客统计、银行收款、商品销售等多方面的报表，让您清晰掌握商城的运营情况，营销推广更高效！'
        },
        {
          introImg: Ds8,
          title: '购物卡折扣卡',
          content:
            '老客户是商城持续发展的重中之重，而维护老客户的秘诀是什么？商城独有的购物卡、折扣卡功能，可以针对特定用户单独发放，是您维护老客户的利器！'
        },
        {
          introImg: Ds9,
          title: '商品订单管理',
          content:
            '商品和订单的管理是一个商城运营的基础，商品分类、标签、属性、库存、图片管理，订单明细、发货、打印、退换货、投诉处理等功能，让您处理业务得心应手！'
        }
      ]
    }
  }
}
</script>
<style lang="less">
.electronics-page {
  .bgcolorF4F4F4 {
    background-color: #f4f4f4;
  }
  .banner_box {
    img {
      display: block;
      width: 100%;
    }
  }
  .mybox {
    padding: 0.8rem 0.333333rem; // 60 25
    .img_box {
      width: 4rem; // 300
      height: 2.4rem; // 180
      vertical-align: top;
      img {
        display: block;
        width: 100%;
        height: 100%;
      }
    }
    .paddingLeft {
      padding-left: 0.266667rem; //20
    }
    .paddingRight {
      padding-right: 0.266667rem; //20
    }
    .text_box {
      width: 5.066667rem; //380
      vertical-align: top;
      .tit {
        padding: 0;
        margin: 0;
        font-size: 0.44rem; //33
        color: #92c3fd;
        line-height: 0.533333rem; //40
        text-align: left;
      }
      .cont {
        padding: 0;
        margin: 0;
        font-size: 0.253333rem; //19
        color: #333333;
        line-height: 0.453333rem;
        text-align: left;
      }
    }
  }
}
</style>
