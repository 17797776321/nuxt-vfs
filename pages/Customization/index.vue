<template>
  <div class="Customization-page">
    <div class="banner_box">
      <img 
        :src="bannerImg" 
        alt="">
    </div>
    <div class="box">
      <div class="tit">APP定制</div>
      <div class="tit_eng">Customization</div>
      <div class="content_box clearfix">
        <div 
          v-for=" (item,index) in customizedData"
          :key="index"
          :class="{'float-left': (index+1)%2 == 1,'float-right':(index+1)%2 == 0,'right':(index+1)%4 == 1,'bottom':((index+1)%4 == 2 && customizedData.length != index+1) || ((index+1)%4 == 3 && customizedData.length != index+1),'left':(index+1)%4 == 0}" 
          class="option_box ">
          <div class="img_box float-left">
            <img 
              :src="item.imgUrl" 
              alt="">
          </div>
          <div class="text_box float-right">
            {{ item.text }}
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import BannerImg from '@/assets/images/banner3.png'

import Cus1 from '@/assets/images/cus1.png'
import Cus2 from '@/assets/images/cus2.png'
import Cus3 from '@/assets/images/cus3.png'
import Cus4 from '@/assets/images/cus4.png'
import Cus5 from '@/assets/images/cus5.png'
import Cus6 from '@/assets/images/cus6.png'
export default {
  name: 'Customization',
  data() {
    return {
      bannerImg: BannerImg,
      customizedData: [
        {
          imgUrl: Cus1,
          text:
            '了解需求分析企业产品市场情况，开展市场调研，编制市场可行性报告。'
        },
        {
          imgUrl: Cus2,
          text: '根据市场调研情况，与企业沟通，策划APP开发及运营方案'
        },
        {
          imgUrl: Cus3,
          text: '设计符合企业文化，产品特色，精致美观，交互性良好的APP界面。'
        },
        {
          imgUrl: Cus4,
          text: '提升用户体验、评估工作量及时间、验收、修改及完善。'
        },
        {
          imgUrl: Cus5,
          text: 'APP开发完成后，加入UI元素，根据测试用户的反馈。'
        },
        {
          imgUrl: Cus6,
          text: '提升用户体验、评估工作量及时间、验收、修改及完善。'
        }
      ]
    }
  }
}
</script>
<style lang="less">
.Customization-page {
  .content_box {
    padding: 0 0.333333rem; //0 25
    .option_box {
      width: 4.16rem; //312
      // height: 1.68rem; //126
      padding: 0.2rem; //15
      box-shadow: 0 0 0.8rem rgba(0, 0, 0, 0.15); // 60
      margin-bottom: 1.266667rem; //95
      .img_box {
        width: 1.053333rem; //79
        height: 1.053333rem; //79
        img {
          display: block;
          width: 100%;
        }
      }
      .text_box {
        width: 2.613333rem; //196
        padding-left: 0.2rem; //15
        font-size: 0.213333rem; //16
        text-align: left;
        color: #333333;
        line-height: 0.346667rem; //26
      }
    }
    .right {
      position: relative;
      &::after {
        display: block;
        content: '';
        width: 0.426667rem; //32
        height: 0.426667rem; //32
        background: url('../../assets/images/right.png') no-repeat;
        background-size: 0.426667rem 0.426667rem;
        position: absolute;
        right: -0.693333rem; //32 +20
        top: 0.586667rem; // 44
      }
    }
    .bottom {
      position: relative;
      &::after {
        display: block;
        content: '';
        width: 0.426667rem; //32
        height: 0.426667rem; //32
        background: url('../../assets/images/bottom.png') no-repeat;
        background-size: 0.426667rem 0.426667rem;
        position: absolute;
        left: 1.786667rem; //134
        bottom: -0.826667rem; //32 + 30
      }
    }
    .left {
      position: relative;
      &::after {
        display: block;
        content: '';
        width: 0.426667rem; //32
        height: 0.426667rem; //32
        background: url('../../assets/images/left.png') no-repeat;
        background-size: 0.426667rem 0.426667rem;
        position: absolute;
        left: -0.693333rem; // 32 + 20
        top: 0.586667rem; //44
      }
    }
  }
}
</style>
