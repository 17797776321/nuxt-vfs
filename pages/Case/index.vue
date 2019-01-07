<template>
  <div class="Case-page">
    <div class="banner_box">
      <img 
        :src="bannerImg" 
        alt="">
    </div>
    <div class="box">
      <div class="tit">客户案例</div>
      <div class="tit_eng">Case</div>
      <a 
        v-for="(item,index) in myCase"
        :key="index"
        :href="item.caseurl" 
        class="card_box">
        <img 
          :src="item.pic" 
          class="img" 
          alt="">
        <div class="tit">{{ item.title }}</div>
        <div class="des">{{ item.des }}</div>
      </a>
    </div>
  </div>
</template>
<script>
import BannerImg from '@/assets/images/banner3.png'
import Axios from 'axios'
export default {
  name: 'Case',
  data() {
    return {
      bannerImg: BannerImg,
      myCase: []
    }
  },
  async asyncData(context) {
    const data = await Axios.get('http://www.vfengs.com/m.php/index/getcases')
    return { myCase: data.data }
  },
  mounted() {}
}
</script>
<style lang="less">
.Case-page {
  .card_box {
    display: block;
    padding: 0.133333rem; //10
    background-color: #ffffff;
    margin-bottom: 0.266667rem; //20
    text-align: left;
    .img {
      display: block;
      width: 100%;
    }
    .tit {
      font-size: 0.32rem; //24
      color: #222222;
      font-size: 0.506667rem; //38
      padding-top: 0.133333rem; //10
    }
    .des {
      font-size: 0.266667rem; //20
      color: #666666;
      line-height: 0.426667rem; //32
    }
  }
}
</style>
