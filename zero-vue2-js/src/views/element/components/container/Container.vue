<!--
 * @Author: Micro-Organism
 * @Date: 2024/8/26 17:29
 * @FilePath: src\views\element\components\container\Container.vue
 * @Email: coolrabbit1993@gmail.com
 * @Description: Container
-->
<script>
export default {
  name: "Container"
}
</script>

<template>
<!-- 用于布局的容器组件，方便快速搭建页面的基本结构：
<el-container>：外层容器。当子元素中包含 <el-header> 或 <el-footer> 时，全部子元素会垂直上下排列，否则会水平左右排列。
<el-header>：顶栏容器。
<el-aside>：侧边栏容器。
<el-main>：主要区域容器。
<el-footer>：底栏容器。
-->
  <el-container>
    <el-header>Header</el-header>
    <el-container>
      <el-aside width="200px">Aside</el-aside>
      <el-main>Main</el-main>
    </el-container>
    <el-footer>Footer</el-footer>
  </el-container>
</template>

<style scoped lang="scss">
.el-header, .el-footer {
  background-color: #B3C0D1;
  color: #333;
  text-align: center;
  line-height: 60px;
}

.el-aside {
  background-color: #D3DCE6;
  color: #333;
  text-align: center;
  line-height: 200px;
}

.el-main {
  background-color: #E9EEF3;
  color: #333;
  text-align: center;
  line-height: 160px;
}

body > .el-container {
  margin-bottom: 40px;
}

.el-container:nth-child(5) .el-aside,
.el-container:nth-child(6) .el-aside {
  line-height: 260px;
}

.el-container:nth-child(7) .el-aside {
  line-height: 320px;
}
</style>
