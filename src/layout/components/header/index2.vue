<template>
  <n-grid h-50 x-gap="12" :cols="4" class="bg-#f6f7f8">
    <n-gi flex items-center>
      <img src="@/assets/images/login_banner.png" height="50" mr10 />
      乐家装饰
    </n-gi>
    <n-gi :span="2" flex items-center justify-center>
      <n-input class="search-input" round placeholder="请输入关键字搜索">
        <template #suffix>
          <n-icon :component="IconSearch" />
        </template>
      </n-input>
    </n-gi>
    <n-gi flex items-center> 咨询热线：13143336946 </n-gi>
  </n-grid>
  <n-menu
    v-model:value="activeKey"
    flex
    items-center
    justify-center
    w-full
    mode="horizontal"
    :options="menuOptions"
    @update:value="handleSelectMenu"
  />
</template>

<script setup>
import { IconSearch } from '@/components/AppIcons'
import { ref, reactive, h } from 'vue'
let activeKey = ref(0)
const menuOptions = reactive([
  {
    label: '主页',
    key: 0,
  },
  {
    label: '品牌简介',
    key: 1,
  },
  {
    label: '设计预约',
    key: 2,
  },
  {
    label: '装修保障',
    key: 3,
  },
  {
    label: '装修攻略',
    key: 4,
  },
  {
    label: '投资合作者关系',
    key: 5,
  },
])
const handleSelectMenu = (value) => {
  console.log(value)
}
</script>

<style lang="scss" scoped>
.search-input {
  &.n-input {
    width: 50%;
  }
}
.n-menu {
  margin: auto;
}
</style>
