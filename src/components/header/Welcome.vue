<template>
  <div class="main" :style="{height:screenHeight+'px',width:screenWidth+'px',backgroundImage:'url('+currentImgUrl+')'}">
    <div class="content">
      <div class="top">
        <h1>Welcome to the!</h1>
      </div>
      <div class="box">
        <div>
          You got to put the past behind you before you can move on.
        </div>
        <div class="icon">
          <div class="item" @click="beforeImg()"><i class="fa fa-angle-left fa-2x"></i></div>
          <div class="item"><i class="fa fa-github-alt fa-2x"></i></div>
          <div class="item"><i class="fa fa-weibo fa-2x"></i></div>
          <div class="item"><i class="fa fa-send fa-2x"></i></div>
          <div class="item"><i class="fa fa-twitter fa-2x"></i></div>
          <div class="item"><i class="fa fa-qq fa-2x"></i></div>
          <div class="item"><i class="fa fa-weixin fa-2x"></i></div>
          <div class="item"><i class="fa fa-envelope fa-2x"></i></div>
          <div class="item" @click="afterImg()"><i class="fa fa-angle-right fa-2x"></i></div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
    export default {
        name: "Welcome",
        data(){
          return{
            currentImg: 0,
            screenWidth: document.documentElement.clientWidth, // 屏幕宽度
            screenHeight: document.documentElement.clientHeight // 屏幕高度
          }
        },
      methods:{
        beforeImg:function () {
          if(this.currentImg<=0){
            this.currentImg=7;
          }else{
            this.currentImg--;
          }
        },
        afterImg:function () {
          if(this.currentImg>=7){
            this.currentImg=0;
          }else{
            this.currentImg++;
          }
        }
      },
      computed:{
        currentImgUrl:function () {
          return "../../static/images/welcome"+this.currentImg+".jpg";
        }
      },
      mounted() {
          setInterval(this.afterImg,10000);
      }
    }
</script>

<style scoped>
  .main{
    width: 100%;
    /*background: url("../../common/images/welcome.jpg") no-repeat;*/
    background-repeat: no-repeat;
    background-size: cover;
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: center;
    /*背景图平滑切换*/
    -moz-transition: all 1s linear 1s;
    -webkit-transition:all 1s linear 1s;
    /*transition:all 1s ease 0s;*/
    -o-transition:all 1s linear 1s;
    transition:all 1s linear 1s;
  }
  .content{
    width: 35%;
    height: 40%;
    margin-top: -10%;
    display: flex;
    flex-direction: column;
    /*justify-content: center;*/
    align-items: center;
  }
  .content .top{
      font-size: 30px;
      color: #fff;
      font-family: 'Ubuntu',sans-serif;
  }
  .content .box{
    height:50px;
    background-color: rgba(0,0,0,.5);
    color: #eaeadf;
    font-size: 16px;
    width: 70%;
    padding: 15px;
    margin-top: 22px;
    line-height: 30px;
    border-radius: 10px;
    box-sizing: initial;
    white-space: nowrap;
    display: flex;
    flex-direction: column;
  }
  .main .box .icon{
    display: flex;
    flex-direction: row;
    justify-content: center;
  }
  .main .icon .item{
    flex: 1;
    display: flex;
    justify-content: center;
    cursor:pointer;
  }
</style>
