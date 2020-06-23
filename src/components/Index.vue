<template>
  <div>
      <topMenu></topMenu>
      <!-- 首页 -->
      <HomePage></HomePage>
      <!-- 个人简介 -->
      <profile></profile>
      <!-- 个人技能 -->
      <skills></skills>
      <!-- 工作经历 -->
      <workExp></workExp>
      <!-- 页脚 -->
      <Footer></Footer>
  </div>
</template>
<script>
import topMenu from './menu/TopMenu'
import profile from './Profile/profile'
import HomePage from './home/HomePage'
import skills from './Skills/skills'
import workExp from './WorkExp/workExp'
import Footer from './Footer/Footer'
export default {
  name: 'Index',
  components: {
    topMenu,
    HomePage,
    profile,
    skills,
    workExp,
    Footer
  }
}
</script>
