<template>
  <div class="container">
    <el-container class="el-container">
      <el-header class="header">
        <el-row :gutter="20">
          <el-col :span="9">
            <div class="grid-content bg-purple">
              <img src="./logo-bai.png" alt="">
            </div>
          </el-col>
          <el-col :span="12">
            <div class="grid-content bg-purple">电商后天管理系统</div>
          </el-col>
          <el-col :span="2">
            <div class="grid-content bg-purple">
              <a href="#">退出</a>
            </div>
          </el-col>
        </el-row>
      </el-header>
      <el-container>
        <el-aside class="aside">Aside</el-aside>
        <el-main class="main">Main</el-main>
      </el-container>
    </el-container>
  </div>
</template>

<script>
export default {};
</script>

<style>
.container,
.el-container {
  height: 100%;
}
.header {
  line-height: 60px;
  background-color: #b3c0d1;
}
.aside {
  width: 200px;
  height: 100%;
  background-color: #d3dce6;
}
.main {
  background-color: #e9eef3;
  height: 100%;
}
</style>