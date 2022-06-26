
<template>
  <el-config-provider size="small" :z-index="3000">
    <div class="app-wrapper">
      <Header />

      <el-container>
        <div class="side-bar">
          <el-menu default-active="1">

            <router-link to="/">
              <el-menu-item index="1">
                <el-icon><icon-home /></el-icon>
                <template #title>Home</template>
              </el-menu-item>
            </router-link>

            <router-link to="/posts">
              <el-menu-item index="2">
                <el-icon><icon-edit /></el-icon>
                <template #title>Posts</template>
              </el-menu-item>
            </router-link>

          </el-menu>
        </div>
        <el-main>
          <router-view />
        </el-main>
      </el-container>

    </div>
  </el-config-provider>
</template>

<script setup lang="ts">
import { ElConfigProvider } from 'element-plus';
import IconHome  from '@/components/icons/IconHome.vue';
import IconEdit from '@/components/icons/IconEdit.vue';
import Header from '@/components/Header.vue';
</script>

<style>
@import '@/assets/base.css';

#app {
  width: 100vw;
  height: 100vh;
  font-weight: normal;
}

.side-bar {
  border: 1px solid red;
  width: 140px;
  height: calc(100vh - 50px);
}
</style>
