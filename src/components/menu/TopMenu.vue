<template>
  <!-- components/TopMenu.vue -->
  <div class="menupage">
    <el-menu
    :default-active="activeIndex"
    class="el-menu-demo"
    mode="horizontal"
    @select="handleSelect"
    background-color="#545c64"
    text-color="#fff"
    active-text-color="#ffd04b">
      <p class="logo-title"><i class="el-icon-user"></i>JEmbrace</p>
      <el-menu-item index="1" style="margin-left:250px;">首页</el-menu-item>
      <el-menu-item index="2">个人简介</el-menu-item>
      <el-menu-item index="3">个人技能</el-menu-item>
      <el-menu-item index="4">工作经历</el-menu-item>
    </el-menu>
  </div>
</template>
<style>
.menupage{
  position: fixed;
  width: 100%;
  top: 0px;
  z-index: 100;
}
.menupage .el-menu.el-menu--horizontal{
  border-bottom: none;
  height: 100px;
  line-height: 100px;
}
.menupage .el-menu.el-menu--horizontal>.el-menu-item,.menupage .el-menu--horizontal>.el-submenu .el-submenu__title{
    height: 100px;
    line-height: 100px;
    padding: 0px 50px;
    font-size: 16px;
    letter-spacing: 4px;
}
.menupage .el-menu--horizontal>.el-menu-item.is-active,.menupage .el-menu--horizontal>.el-submenu.is-active .el-submenu__title{
  border-bottom-width: 4px;
}
.menupage .logo-title .el-icon-user{
  margin-right: 5px;
}
</style>
<style scoped>
  .logo-title{
    position: absolute;
    left: 100px;
    top: 0px;
    color:#fff;
    font-size:26px;
    cursor: pointer;
  }
  .logo-title img{
    width: 80px;
    outline:none;
    vertical-align: middle;
  }
</style>
<script>
export default {
  name: 'topMenu',
  data () {
    return {
      activeIndex: '1'
    }
  },
  methods: {
    // 点击菜单栏的选择，自动滚动到对应的视图
    handleSelect (index, indexPath) {
      var name = ''
      if (index === '1') name = 'homepage'
      if (index === '4') name = 'productpage'
      if (index === '3') name = 'securityresearch'
      if (index === '2') name = 'aboutus'
      var targetEle = document.querySelector('.' + name)
      var offsetTop = targetEle.offsetTop
      document.documentElement.scrollTop = offsetTop - 150
    }
  }
}
</script>
