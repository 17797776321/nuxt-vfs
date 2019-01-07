<template>
  <div class="website-page">
    <div class="banner_box">
      <img 
        :src="bannerImg" 
        alt="">
    </div>
    <div class="box">
      <div class="tit">网站建设</div>
      <div class="tit_eng">Website</div>
      <div class="option_box clearfix">
        <div 
          v-for="(item,index) in websiteArr"
          :key="index"
          :class="{'float-left': (index+1)%2 == 1,'float-right': (index+1)%2 == 0}" 
          :style="{'backgroundColor': item.color}" 
          class="option">
          <div class="tit_box">
            <img 
              :src="item.imgUrl" 
              alt="">
            <span>{{ item.title }}</span>
          </div>
          <div class="des_box">
            {{ item.content }}
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import BannerImg from '@/assets/images/banner3.png'

import Web1 from '@/assets/images/web1.png'
import Web2 from '@/assets/images/web2.png'
import Web3 from '@/assets/images/web3.png'
import Web4 from '@/assets/images/web4.png'
import Web5 from '@/assets/images/web5.png'
import Web6 from '@/assets/images/web6.png'
export default {
  name: 'Website',
  data() {
    return {
      bannerImg: BannerImg,
      websiteArr: [
        {
          imgUrl: Web1,
          title: '网站规划',
          content:
            '定位建议分析，网站栏目架构设计、网站规划布局结构，整套解决方案。',
          color: '#F27B53'
        },
        {
          imgUrl: Web2,
          title: '网页设计',
          content:
            '美术创意设计、专业形象界面设计、CSS+DIV前台结构布局设计、SEO优化。',
          color: '#0CAED4'
        },
        {
          imgUrl: Web3,
          title: '域名、邮箱',
          content: '域名、邮箱规划配置。',
          color: '#75B749'
        },
        {
          imgUrl: Web4,
          title: '网站系统功能开发',
          content: '系统性架构策略、程序模块功能分析设计、安全策略。',
          color: '#FFB400'
        },
        {
          imgUrl: Web5,
          title: '网站运营维护方案',
          content:
            '根据品牌宣传网站管理模式，建议网站日常信息提供、审核、发布的一整套运转方案，网站培训及知识转移计划等。',
          color: '#DE567A'
        },
        {
          imgUrl: Web6,
          title: '网站营销推广计划',
          content: '网站运维策略及网站价值分析、盈利情况分析等等...',
          color: '#E75708'
        }
      ]
    }
  }
}
</script>
<style lang="less">
.website-page {
  .option_box {
    padding: 0 0.333333rem; // 0 25
    .option {
      width: 4.6rem; //345
      height: 2.866667rem; //215
      text-align: left;
      color: #ffffff;
      margin-top: 0.133333rem; // 10
      .tit_box {
        padding: 0.24rem; //18
        img {
          display: inline-block;
          width: 1.16rem; //87
          vertical-align: bottom;
        }
        span {
          display: inline-block;
          font-size: 0.333333rem; //25
          padding-left: 0.16rem; //12
          vertical-align: bottom;
        }
      }
      .des_box {
        padding: 0.066667rem 0.266667rem; // 5 20
        font-size: 0.213333rem; //16
        line-height: 0.373333rem; //28
      }
    }
  }
}
</style>
