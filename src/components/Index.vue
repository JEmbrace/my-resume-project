<template>
  <div>
      <topMenu></topMenu>
      <!-- 首页 -->
      <HomePage></HomePage>
      <!-- 个人简介 -->
      <AboutUs></AboutUs>
      <!-- 个人技能 -->
      <SecurityResearch></SecurityResearch>
      <!-- 工作经历 -->
      <Products></Products>
      <!-- 页脚 -->
      <Footer></Footer>
  </div>
</template>
<script>
import topMenu from './menu/TopMenu'
import AboutUs from './AboutUs/AboutUs'
import HomePage from './home/HomePage'
import Products from './product/Products'
import SecurityResearch from './SecurityResearch/SecurityResearch'
import Footer from './Footer/Footer'
export default {
  name: 'Index',
  components: {
    topMenu,
    HomePage,
    Products,
    SecurityResearch,
    AboutUs,
    Footer
  }
}
</script>
