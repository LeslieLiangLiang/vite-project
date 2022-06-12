<template>
  <n-layout max-w-1200 mx-auto>
    <!-- <n-layout-sider
      bordered
      collapse-mode="width"
      :collapsed-width="64"
      :width="220"
      :native-scrollbar="false"
      :collapsed="appStore.collapsed"
    >
      <SideBar />
    </n-layout-sider> -->
    <n-layout-header>
      <AppHeader />
    </n-layout-header>

    <n-layout style="background-color: #f5f6fb" :style="`height: calc(100% - 50px)`">
      <!-- <AppTags v-if="useTheme.tags.visible" /> -->
      <AppMain

      />
    </n-layout>
  </n-layout>
</template>

<script setup>
import AppHeader from './components/header/index2.vue'
import SideBar from './components/sidebar/index.vue'
import AppMain from './components/AppMain.vue'
import AppTags from './components/tags/index.vue'
import { useThemeStore } from '@/store/modules/theme'
import { useAppStore } from '@/store/modules/app'

const useTheme = useThemeStore()
const appStore = useAppStore()
</script>

<style lang="scss" scoped></style>
