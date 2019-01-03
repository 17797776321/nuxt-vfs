<template>
  <div class="footer-component">
    <p class="text">
      邮箱：66378@qq.com
    </p>
    <p class="text">
      电话：400-816-7772
    </p>
    <p class="text">
      地址：郑州市郑东新区绿地之窗景峰座
    </p>
    <a 
      href="javascript:void(0);" 
      class="mybtn">联系我们</a>
  </div>
</template>
<script>
export default {
  name: 'Footer',
  data() {
    return {}
  }
}
</script>
<style lang="less">
.footer-component {
  padding: 27px 45px;
  background-color: #333333;
  .text {
    margin: 0;
    font-size: 30px;
    color: #9ba0a3;
    line-height: 44px;
  }
  .mybtn {
    display: inline-block;
    width: 200px;
    background-color: #ff5c46;
    font-size: 30px;
    color: #ffffff;
    text-align: center;
    line-height: 70px;
    margin-top: 40px;
  }
}
</style>
