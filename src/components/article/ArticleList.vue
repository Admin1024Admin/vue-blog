<template>
  <div class="main">
    <div class="item_left"></div>
    <div class="item_center">
      <!--公告-->
      <div class="prompt">
        <i class="fa fa-volume-up fa-fw"></i>&nbsp;&nbsp;最近事多，评论无法逐一回复，见谅~>ω<
      </div>
      <!--标题-->
      <div class="title">
        <i class="fa fa-leaf fa-fw"></i>&nbsp;&nbsp;Discovery
      </div>
      <!--文章列表-->
      <div class="list">
        <div class="item"></div>
        <div class="item"></div>
        <div class="item"></div>
        <div class="item"></div>
        <div class="item"></div>
        <div class="item"></div>
        <div class="item"></div>
        <div class="item"></div>
        <div class="item"></div>
        <div class="item"></div>
      </div>
      <!--下一页-->
      <div class="next_page">
        Previous
      </div>
      <!--页脚-->
      <div class="font">
        <span>Crafted with  by Mashiro</span>
        <span style="font-size: 14px;color:#999;">© 2019 樱花庄的白猫 沪ICP备17028213号</span>
        <p id="footer-sponsor">
          <a href="https://console.upyun.com/register/?invite=r1EuSLN-f" target="_blank" alt="CDN Sponsor" rel="nofollow">
            <img src="https://cdn.jsdelivr.net/gh/moezx/cdn@3.0.8/img/logo/upyun.png" alt="CDN Sponsor" style="height: 2em; max-height: 2em;"></a>&nbsp;&nbsp;&nbsp;
          <a href="http://www.vultr.com/?ref=7196564" target="_blank" alt="Server provider" rel="nofollow">
            <img src="https://cdn.jsdelivr.net/gh/moezx/cdn@3.0.8/img/logo/logo_onwhite.png" alt="Server provider" style="height: 1.3em; max-height: 1.3em;padding-bottom: 0px;margin-bottom: 0.35em;"></a>&nbsp;&nbsp;&nbsp;
          <a href="https://www.jsdelivr.com/" target="_blank" alt="Free CDN" rel="nofollow">
            <img src="https://cdn.jsdelivr.net/gh/moezx/cdn@3.0.8/img/logo/JsDelivr_Logo.svg" alt="jsDelivr" style="height: 2em; max-height: 2em;padding-bottom: 0px;"></a>&nbsp;&nbsp;&nbsp;
          <a href="https://www.google.com/intl/ja/analytics/" target="_blank" alt="Analytics solution" rel="nofollow">
            <img src="https://cdn.jsdelivr.net/gh/moezx/cdn@3.0.8/img/logo/Google.svg" alt="Google Analytics" style="height: 1.7em; max-height: 1.7em;padding-bottom: 0px;"></a>
        </p>
      </div>
    </div>
    <div class="item_right"></div>
  </div>
</template>

<script>
    export default {
        name: "ArticleList"
    }
</script>

<style scoped>
  .main{
    height: auto;
    width: 100%;
    display: flex;
    flex-direction: row;
  }
  .main .item_left,.item_right{
    flex: 1;
  }
  .main .item_center{
    flex: 2;
    /*border: 1px blue solid;*/
    display: flex;
    flex-direction: column;
    /*justify-content: center;*/
    align-items: center;
    background:rgba(255,255,255,.8);;
  }
  .main .item_center .prompt{
    margin-top: 40px;
    width: 96%;
    border:1px #999 dashed;
    border-radius: 5px;
    color:#999;
    padding:20px 5px;
  }
  .main .item_center .title{
    width: 96%;
    height: auto;
    color:#999;
    margin-top:20px;
    padding: 5px;
    border-bottom: 1px #999 dashed;
  }
  .main .item_center .list{
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    width: 96%;
    height: auto;
  }
  .main .item_center .list .item{
    flex: 1;
    height: 300px;
    width:100%;
    margin-top: 20px;
    margin-bottom: 20px;
    border-radius: 10px;
    background-color: rgba(255,255,255,0);
    box-shadow: 0 5px 10px 5px rgba(110,110,110,.4);
  }
  .main .item_center .next_page{
    width:140px;
    height:50px;
    border:1px #ccc solid;
    border-radius: 30px;
    margin-top: 30px;
    font-size: 20px;
    color: #999;
    font-weight: 200;
    font-family: 方正姚体;
    display: flex;
    justify-content: center;
    align-items: center;
  }
  .main .item_center .font{
    width: 96%;
    height:200px;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    font-size: 12px;
    line-height: 30px;
  }
</style>
