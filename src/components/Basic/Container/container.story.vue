<script setup lang="ts">
const headerHeight = ref(60)
const footerHeight = ref(60)
const asideWidth = ref(100)
</script>

<template>
  <Story title="Basic/Container" icon="ph:layout-thin">
    <Variant title="Basic Usage" >
        <el-container>
          <el-header :height="`${headerHeight}px`">
            Header
          </el-header>
          <el-container>
            <el-aside :width="`${asideWidth}px`">
              Aside
            </el-aside>
            <el-container>
              <el-main>Main</el-main>
              <el-footer :height="`${footerHeight}px`">
                Footer
              </el-footer>
            </el-container>
          </el-container>
        </el-container>
      <template #controls>
        <HstNumber v-model="headerHeight" title="HeaderHeight" />
        <HstNumber v-model="footerHeight" title="FooterHeight" />
        <HstNumber v-model="asideWidth" title="AsideWidth" />
      </template>
    </Variant>
  </Story>
</template>

<style scoped>
  .el-header, .el-footer {
    background-color: #c6e2ff;
    color: #333;
    text-align: center;
    line-height: 60px;
  }

  .el-aside {
    background-color: #d9ecff;
    color: #333;
    text-align: center;
    line-height: 200px;
  }

  .el-main {
    background-color: #ecf5ff;
    color: #333;
    text-align: center;
    line-height: 160px;
  }
</style>
