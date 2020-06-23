<template>
  <div class="skills">
      <div class="title">
        <el-divider content-position="center">个人技能</el-divider>
        <p><el-tag>vue全家桶</el-tag><el-tag >javascript</el-tag><el-tag>css</el-tag></p>
      </div>
      <div class="skill">
        <span class='vue'>Vue</span>
        <span class='js'>JS</span>
        <span class='css'>CSS</span>
        <span class='echarts'>Echarts</span>
        <span class='webpack'>webpack</span>
        <span class='python'>python</span>
        <span class='linux'>linux</span>
      </div>
  </div>
</template>
<style>
  .skills .title p .el-tag{
    margin: 0px 5px;
    cursor: pointer;
  }
  .skills .box-card .text{
    text-align: left;
  }
</style>
<style scoped>
  .skills{
    font-size: 14px;
    padding: 0px 100px;
  }
  .title p{
    color: #8c8888;
    font-size: 15px;
    margin-bottom: 80px;
    text-align: center;
  }
  .content p{
    font-size: 20px;
    color: #8c8888;
  }
  .skill{
    margin: 100px 0px;
    position: relative;
  }
  .skill span{
    display: inline-block;
    color: #fff;
    border-radius: 50%;
  }
  span.vue{
    background-color: rgba(102,153,204,1) ;
    width: 200px;
    height: 200px;
    line-height: 200px;
    font-size: 28px;
    z-index: 100;
  }
  span.js{
    background-color: rgba(255,153,102,0.5);
    width: 130px;
    height: 130px;
    line-height: 130px;
    font-size: 26px;
    position: absolute;
    left: 43%;
    bottom: 150px;
    z-index: 0;
  }
  span.css{
    background-color: rgba(102,204,204,0.8);
    width: 90px;
    height: 90px;
    font-size: 26px;
    line-height: 90px;
    font-size: 26px;
    position: absolute;
    left: 35%;
    top: 100px;
    z-index: 0;
  }
  span.echarts{
    background-color: rgba(255,153,153,0.7) ;
    width: 100px;
    height: 100px;
    line-height: 100px;
    font-size: 24px;
    position: absolute;
    left: 59%;
    bottom: 10px;
    z-index: 0;
  }
  span.webpack{
    background-color: rgba(255,204,51,0.8);
    width: 70px;
    height: 70px;
    line-height: 70px;
    font-size: 13px;
    position: absolute;
    left: 30%;
    top: 20px;
    z-index: 0;
  }
  span.python{
    background-color: rgba(204,102,102,0.5) ;
    width: 60px;
    height: 60px;
    line-height: 60px;
    font-size: 14px;
    position: absolute;
    left: 51%;
    bottom: -10px;
    z-index: 0;
  }
  span.linux{
    background-color: rgba(153,153,255,0.8) ;
    width: 60px;
    height: 60px;
    line-height: 60px;
    font-size: 14px;
    position: absolute;
    left: 60%;
    top: -50px;
    z-index: 0;
  }
</style>
<script>
export default {
  name: 'Skills'
}
</script>
