<template>
  <div class="aboutus">
    <div class="title">
      <el-divider content-position="center">个人简介</el-divider>
      <p><el-tag>xxxx大学</el-tag><el-tag>本科</el-tag></p>
    </div>
    <el-card class="box-card" style="margin-bottom: 20px;">
      <div class="text item">
        <el-row :gutter="110">
          <el-col :span="8">
            <div class="grid-content bg-purple">
              于2005.07月毕业于<span class="large">某喵喵喵大学</span>，本科学历。在校专业为xxxxxxx，主修课程为xxxx、xxxx、xx和xxxx等课程。在校期间主要技能为java和php语言,和实验室小伙伴一起完成过内部管理平台(成员在线时长记录、周计划制定和组长评价)、纳新面试系统等。
            </div>
          </el-col>
          <el-col :span="8">
            <div class="grid-content bg-purple">
                毕业后在某某公司做web开发工作,主要的技能为css、javascript、jquery和python。主要参与的产品有xxxxxxx、xxxx。现就职于一家创业公司做web前端岗位，主要的技能为vue全家桶。
            </div>
          </el-col>
          <el-col :span="8">
            <div class="grid-content bg-purple">
                工作中比较自律，对待工作认真负责，喜欢<span class="large">不断学习</span>来提升自己。希望能找到一群志同道合的人一起工作，不断进步和成长。
            </div>
          </el-col>
        </el-row>
      </div>
      <div class='topMask square'></div><div class='topMask circular'></div>
    </el-card>
  </div>
</template>
<script>
export default {
  name: 'AboutUs'
}
</script>
<style>
  .aboutus .grid-content.line{
    border-right: 1px solid #ddd;
    height: 150px;
  }
  .aboutus .el-card__header{
    background: #545c64;
  }
  .aboutus .el-card__body{
    padding: 50px 20px;
  }
  .aboutus .el-timeline-item__wrapper{
    top: -8px;
  }
  .aboutus .title p .el-tag{
    margin: 0px 5px;
    cursor: pointer;
  }
</style>
<style scoped>
  .aboutus{
    font-size: 14px;
    text-align: left;
    padding: 0px 100px;
  }
  .intro{
    width: 200px;
    border: 1px solid #ddd;
    border-radius: 5px;
  }
  .text {
    font-size: 14px;
    text-align: left;
    line-height: 30px;
    text-indent: 2em;
  }
  .box-card{
    position: relative;
  }
  .item {
    display: inline-block;
    margin: 30px 50px;
  }
  .clearfix:before,
  .clearfix:after {
    display: table;
    content: "";
  }
  .clearfix:after {
    clear: both
  }
  .clearfix span{
    color: #fff;
    font-weight: bold;
  }
  .title p{
    color: #8c8888;
    font-size: 15px;
    margin-bottom: 80px;
    text-align: center;
  }
  .grid-content .large{
    font-size: 16px;
    color: #409EFF;
    font-weight: bold;
  }
  .topMask{
    width: 100px;
    height: 100px;
    background-color: rgba(68,138,255,0.2);
    transform: rotate(45deg);
    position: absolute;
  }
  .square{
    border-radius: 5px;
    top: 0px;
  }
  .circular{
    border-radius: 50%;
    top:80px;
    left: 80%;
    background-color: rgba(255, 208, 75,0.2);
  }
</style>
