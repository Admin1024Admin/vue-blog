<template>
  <div style="position: fixed;top: 0px;height: auto;width: 100%;">
    <div class="main">
      <div class="icon"><span class="text">さ阿娇爱上了阿强</span></div>
      <div class="nav">
        <div class="item"><i class="fa fa-home fa-fw"></i>首页</div>
        <div class="item"><i class="fa fa-book fa-fw"></i>归档</div>
        <div class="item"><i class="fa fa-navicon  fa-fw"></i>清单</div>
        <div class="item"><i class="fa fa-commenting fa-fw"></i>留言板</div>
        <div class="item"><i class="fa fa-heart fa-fw"></i>赞善</div>
        <div class="item"><i class="fa fa-leaf fa-fw"></i>关于</div>
        <div class="item"><i class="fa fa-android fa-fw"></i>客户端</div>
      </div>
      <div class="zw"></div>
      <div class="user">
        <span><i class="fa fa-search fa-fw"></i></span>
        <span><i class="fa fa-user-o fa-fw"></i></span>
      </div>
    </div>
  </div>

</template>

<script>
    export default {
        name: "NavBar"
    }
</script>

<style scoped>
  .main{
    display: flex;
    flex-direction: row;
    height:50px;
    background:rgba(255,255,255,.95);
    border-bottom: 1px #ccc solid;
  }
  .main .icon{
    font-size: 30px;
    flex: 2;
    padding-left: 100px;
  }
  .icon:nth-child(2){
    font-family: 方正姚体;
    color:red;
  }
  .main .nav{
    flex: 6;
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: center;
  }
  .main .nav .item{
    flex: 1;
    /*line-height:50px;*/
    font-size: 20px;
    font-family: 华文楷体;
  }
  .main .zw{
    flex:2;
  }
  .main .user{
    flex: 1;
    display: flex;
    flex-direction: row;
    /*justify-content: center;*/
    align-items: center;
  }
  .main .user span{
    margin-left: 20px;
    color:#999;
    font-size: 22px;
  }
  .text{
    background-image: -webkit-linear-gradient(left,yellow,#66ffff 10%, #adffc1 20%, #7dcc7f 30%, #CCCCFF 40%, #00FFFF 50%,#CCCCFF 60%,#CC00CC 70%,#CC00FF 80%,#66FFFF 90%,blue 100%);
    -webkit-text-fill-color: transparent;/* 将字体设置成透明色 */
    -webkit-background-clip: text;/* 裁剪背景图，使文字作为裁剪区域向外裁剪 */
    -webkit-background-size: 200% 100%;
    -webkit-animation: masked-animation 4s linear infinite;
  }
  @keyframes masked-animation {
    0% {
      background-position: 0 0;
    }
    100% {
      background-position: -100% 0;
    }
  }
</style>
