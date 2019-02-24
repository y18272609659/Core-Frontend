<template>
  <div>
    <div class="suburb-wrapper">
        <!--郊外页面页头-->
        <div class="suburb-header">
          <div class="logo-wrapper">
            <img class="logo" src="../assets/logo.png" alt="">
          </div>
          <div class="suburb-title" @click="jump('manor')" style="cursor: pointer">{{ kingdom }}</div>
        </div>
        <div class="suburb-content">
          <!--商会接头人-->
          <div class="black-market">
            <img class="businessman-img" src="../../static/昂尼森商会接头人.png"/>
            <div class="businessman-name">
              <span class="organize">昂尼森商会</span>
              <span class="name">接头人</span>
            </div>
          </div>
          <!--说明&选择框-->
          <div class="suburb-choose">
            <div class="explain">
              <p>你来到了这片荒芜的郊外，两个略显寂寥的人站在远处，却又彼此远离。</p>
              <p>这一幕落在你的眼中，要去跟他们搭话吗？</p>
            </div>
            <button class="say-businessman orange-button">跟商会接头人聊聊</button>
            <button class="say-soldier dodgerblue-button">找这位老兵聊一聊</button>
          </div>
          <!--老兵联络人-->
          <div class="soldier">
            <img class="soldier-img" src="../../static/老兵协会联络人.png"/>
            <div class="soldier-name">
              <span class="organize">老兵协会</span>
              <span class="name">联络人</span>
            </div>
          </div>
      </div>
      <!--按钮列表-->
      <div class="links-wrapper">
        <button class="link" @click="jump('building')">建筑</button>
        <button class="link" @click="jump('plat')">地图</button>
        <button class="link" @click="jump('#')">军事</button>
        <button class="link" @click="jump('suburb')">郊外</button>
      </div>
    </div>
    <Vfooter/>
  </div>
</template>

<script>
  import Vfooter from './sub/v-footer'
  export default {
    name: 'suburb',
    components: {Vfooter},
    computed: {
      kingdom () {
        return this.$store.state.kingdom
      }
    },
    created () {
      // 赋值用户数据
      this.setUser()
    }
  }
</script>

<style lang="scss" scoped>
  @import "../assets/scss/global_css";
  .suburb-wrapper {
    width: 100%;
    min-height: 87.88vh;
  }
  // header部分布局
  .suburb-header {
    padding: 0 0 40px 0;
  }
  .suburb-header .logo, .logo-wrapper, .suburb-title {
    display: inline-block;
  }
  .logo-wrapper {
    float: left;
    margin: 3vw 0 0 4vw;
  }
  .logo {
    width: 300px;
  }
  .suburb-title {
    margin: 3vw 0 0 -26vw;
    font-size: 2.8rem;
  }
  // 功能部分布局
  .suburb-content {
    display: inline-flex;
    flex-direction: row;
    justify-content: space-around;
  }
  .suburb-content .black-market, .suburb-choose, .soldier {
    width: 32vw;
    min-height: 300px;
    /*background: orange;*/
  }
  // 商会接头人
  .businessman-img {
    margin: 1vw 0 0 -10vw;
  }
  .businessman-name {
    margin-left: 5.5vw;
    width: 140px;
    height: 60px;
    background: rgba(0, 0, 0, 0.8);
    border-radius: 5px;
  }
  .businessman-name .organize {
    display: block;
    font-size: 1.3rem;
    font-weight: bold;
    color: orange;
    /*text-shadow: 1px 1px 1px gray;*/
    -webkit-text-stroke: 0.7px black;
  }
  .businessman-name .name {
    display: block;
    font-size: 1rem;
    font-weight: bold;
    color: white;
    -webkit-text-stroke: 0.6px black;
  }
  // 旁白与对话按钮部分
  .suburb-choose {
    width: 32vw;
    min-height: 300px;
    background: #e6e6e6;
    font-size: 1rem;
  }
  .suburb-choose p {
    margin: 0 4vw;
    width: 24vw;
    padding-top: 30px;
    line-height: 1.5rem;
    text-align: left;
  }
  .suburb-choose button {
    width: 20vw;
    height: 30px;
    margin: 20px auto;
    display: block;
    font-size: 0.8rem;
  }
  // 老兵联络人（样式类似于商会接头人）
  .soldier-img {
    margin: 9vw 0 0 4vw;
  }
  .soldier-name {
    margin-left: 13vw;
    width: 140px;
    height: 60px;
    background: rgba(0, 0, 0, 0.8);
    border-radius: 5px;
  }
  .soldier-name .organize {
    display: block;
    font-size: 1.3rem;
    font-weight: bold;
    color: dodgerblue;
    -webkit-text-stroke: 0.7px black;
  }
  .soldier-name .name {
    display: block;
    font-size: 1rem;
    font-weight: bold;
    color: white;
    -webkit-text-stroke: 0.6px black;
  }
  /*按钮列表*/
  .links-wrapper {
    min-height: 80px;
    margin-top: 20px;
  }
  .links-wrapper button {
    margin: 0 20px 0 20px;
  }
</style>
