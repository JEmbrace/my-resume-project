<template>
  <div class='footer'>
      <span class="scroll"></span>
      <el-divider></el-divider>
      <span>法律声明</span>
      <el-divider direction="vertical"></el-divider>
      <span>友情链接</span>
      <el-divider direction="vertical"></el-divider>
      <span @click="drawer = true">联系我</span>
      <br/>
      <br/>
      <span class="copyright">版权所有 JEmbrace</span>
      <el-drawer
        title="联系我"
        :visible.sync="drawer"
        :direction="direction"
        :before-close="handleClose">
        <p class='info'>
          <i class="el-icon-phone"></i>电话：18822299999<br/>
          <i class="el-icon-message"></i>邮箱：18822299999@163.com<br/>
          <i class="el-icon-message"></i>博客：https://www.cnblogs.com/HouJiao/<br/>
          <i class="el-icon-message"></i>github：https://github.com/JEmbrace<br/>
        </p>
      </el-drawer>
  </div>
</template>
<style>
  .el-divider{
    background-color: rgb(84, 92, 100);
  }
</style>
<style scoped>
    .footer{
        height: 250px;
        text-align: center;
        font-size: 16px;
        padding: 0px 100px;
        position: relative;
    }
    .footer{
      cursor: pointer;
    }
    .copyright{
      font-size: 12px;
    }
    .info{
      font-size: 14px;
      color: #72767b;
      line-height: 25px;
    }
    .footer .scroll{
      display: inline-block;
      width: 20px;
      height: 20px;
      border-radius: 5px;
      border:1px solid #448aff;
      background-color: rgba(68,138,255,0.2);
      position: absolute;
      left: 5%;
      top: -25px;
      z-index: 10;
      animation: scrollA infinite 20s linear alternate;
    }
    @keyframes scrollA {
      0% {left: 5%;transform: rotate(180deg);};
      10% {left: 5%;transform: rotate(270deg);}
      20% {left: 5%;transform: rotate(450deg);}
      25% {left: 10%;transform: rotate(540deg);}
      30% {left: 20%;transform: rotate(720deg);}
      35% {left: 30%;transform: rotate(900deg);}
      40% {left: 40%;transform: rotate(1080deg);}
      45% {left: 50%;transform: rotate(1260deg);}
      50% {left: 60%;transform: rotate(1440deg);}
      55% {left: 70%;transform: rotate(1620deg);}
      60% {left: 80%;transform: rotate(1800deg);}
      80% {left: 90%;transform: rotate(2610deg);}
      90% {left: 90%;transform: rotate(2340deg);}
      100% {left: 90%;transform: rotate(2520deg);}
    }
</style>
<script>
export default {
  name: 'Footer',
  data () {
    return {
      drawer: false,
      direction: 'btt'
    }
  },
  methods: {
    handleClose (done) {
      done()
    }
  }
}
/*
*1.要想修改element组件的样式，需要将样式写在没有scoped修饰的stype标签内部，这样自定义的样式才能生效。
*再者，假如该样式可应用于所有组件，css选择器直接选中组件类名或者id名，无需添加父级选择器进行限制；
*假如该样式只应用于本组件，css选择器的范围一定要在本组件内，在选中需要修改的组件的类型或者id名，这样在父选择器的限制下，样式不会影响其他组件。
*/
</script>
