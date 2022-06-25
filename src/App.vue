
<template>
  <el-config-provider size="small" :z-index="3000">
    <div class="app-wrapper">
      <el-header class="header">Header</el-header>

      <el-container>
        <div class="side-bar">
          <el-menu default-active="1">
            <el-menu-item index="1">
              <el-icon>
                <location />
              </el-icon>
              <template #title>Home</template>
            </el-menu-item>
            <el-menu-item index="2">
              <el-icon>
                <location />
              </el-icon>
              <template #title>Posts</template>
            </el-menu-item>
          </el-menu>
        </div>
        <el-main>Main Content</el-main>
      </el-container>


    </div>
  </el-config-provider>
</template>

<script setup lang="ts">
import { ElConfigProvider } from 'element-plus';
</script>

<style>
@import '@/assets/base.css';

#app {
  width: 100vw;
  height: 100vh;
  font-weight: normal;
}

.header {
  line-height: 1.5;
  height: 50px;
  border: 1px solid red;
}

.side-bar {
  border: 1px solid red;
  width: 140px;
  height: calc(100vh - 50px);
}
</style>
