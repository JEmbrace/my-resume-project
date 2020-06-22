<template>
  <div class="productpage">
    <div class="title">
      <el-divider content-position="center">工作经历</el-divider>
      <p><el-tag >某司</el-tag><el-tag>某某司</el-tag></p>
    </div>
    <div class='experience'>
      <el-timeline>
        <el-timeline-item timestamp="2010/07/-2014/10" placement="top">
          <el-card>
            <h4>某司</h4>
            <p>
              主要负责某某产品、某某某产品的前端开发和部分后端功能开发<br>
              产品bug修复<br>
              产品前场问题反馈处理<br>
            </p>
          </el-card>
        </el-timeline-item>
        <el-timeline-item timestamp="2014/10-至今" placement="top">
          <el-card>
            <h4>xxx</h4>
            <p>xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx</p>
          </el-card>
        </el-timeline-item>
      </el-timeline>
    </div>
    <div class="project">
      <div class="content" @click="drawerHander(1)" >
          <img src='../../assets/p1.jpg' class='ifns'>
          <div class='hover'>
            <p>项目1</p>
          </div>
      </div>
      <div class="content" @click="drawerHander(2)">
        <img src='../../assets/p1.jpg' class='ifns'>
        <div class='hover'>
        <p>项目2</p>
        </div>
      </div>
      <div class="content" @click="drawerHander(3)">
        <img src='../../assets/p1.jpg' class='ifns'>
        <div class='hover'>
          <p>项目3</p>
        </div>
      </div>
    </div>
    <el-drawer
      :title="projectInfo[currentIndex]['title']"
      :visible.sync="drawer"
      :direction="direction"
      :before-close="handleClose">
        <p class='info'>
          <el-row>
            <el-col :span="24">
              <div class="grid-content bg-purple-dark">
                项目介绍：{{projectInfo[currentIndex]['intro']}}
              </div>
            </el-col>
          </el-row>
          <el-row>
            <el-col :span="24">
              <div class="grid-content bg-purple-dark">
                所在公司：{{projectInfo[currentIndex]['company']}}
              </div>
            </el-col>
          </el-row>
          <el-row>
            <el-col :span="24">
              <div class="grid-content bg-purple-dark">
                开发环境：{{projectInfo[currentIndex]['developEnv']}}
              </div>
            </el-col>
          </el-row>
          <el-row>
            <el-col :span="24">
              <div class="grid-content bg-purple-dark">
                职责描述:
              </div>
              <div class="grid-content bg-purple-dark" v-for="(item,key) in projectInfo[currentIndex]['responsibility']" :key="key">
                {{projectInfo[currentIndex]['responsibility'][key]}}
              </div>
            </el-col>
          </el-row>
        </p>
    </el-drawer>
  </div>
</template>

<script>
export default {
  name: 'Products',
  data () {
    return {
      drawer: false,
      direction: 'btt',
      currentIndex: 0,
      projectInfo: [
        {
          title: '项目1',
          intro: '这里是项目介绍',
          company: '某司',
          developEnv: '这里是开发环境介绍',
          responsibility: {
            res1: '职责1',
            res2: '职责2',
            res3: '职责3'
          }
        }, {
          title: '项目2',
          intro: '这里是项目2介绍',
          company: '某司',
          developEnv: '这里是开发环境介绍',
          responsibility: {
            res1: '职责1',
            res2: '职责2',
            res3: '职责3'
          }
        }, {
          title: '项目3',
          intro: '这里是项目3介绍',
          company: '某司',
          developEnv: '这里是开发环境介绍',
          responsibility: {
            res1: '职责1',
            res2: '职责2',
            res3: '职责3'
          }
        }
      ]
    }
  },
  methods: {
    handleClose (done) {
      done()
    },
    drawerHander (index) {
      this.drawer = true
      this.currentIndex = index - 1
    }
  }
}
</script>
<style>
  div .el-divider--horizontal{
    height: 2px;
    margin-top:100px;
    background-color: rgb(84, 92, 100);
  }
  div .el-divider__text{
    font-size: 26px;
    color: #545c64;
  }
  div .el-drawer__header{
    font-size: 20px;
    font-weight: blod;
    padding-bottom: 20px;
    border-bottom: 1px solid;
  }
  div .el-drawer{
    background-color: rgb(61, 67, 72);
    color: #ccc;
  }
  div .el-drawer__body{
    padding: 0px 20px 0px 20px;
  }
</style>
<style scoped>
  .productpage{
    padding: 0px 100px 0px 100px;
  }
  .productpage .project{
    display: flex;
    justify-content:space-around;
  }
  .ifns{
    width:85%;
    display: inline-block;
    outline: 1px dashed rgba(84, 92, 100, 0.1);
  }
  .experience{
    text-align: left;
  }
  .content{
    text-align: center;
    display: inline;
    position: relative;
    margin: 20px;
  }
  .content p{
    width: 95%;
    color: #fff;
    font-size: 14px;
    text-align: center;
  }
  .hover{
    position: absolute;
    bottom: 5px;
    left: 7.5%;
    background-color: rgba(84, 92, 100, 0.3);
    height: 60px;
    width: 85%;
    line-height: 60px;
    cursor: pointer;
  }
  .hover:hover{
    background-color: rgba(84, 92, 100, 0.6);
  }
  h1{
    border:1px solid #ccc;
    height: 0px;
  }
  .title p{
    color: #8c8888;
    font-size: 15px;
    margin-top: 30px;
    margin-bottom: 20px;
  }
  .title p .el-tag{
    margin: 0px 5px;
    cursor: pointer;
  }
  .info{
    font-size: 14px;
    color: #72767b;
    line-height: 25px;
  }
</style>
