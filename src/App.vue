<script setup lang="ts">
import { defineAsyncComponent } from "vue";
const PageHeader = defineAsyncComponent(() => import("./components/common/header/PageHeader.vue"));
const PageBody = defineAsyncComponent(() => import("./components/common/body/PageBody.vue"));
const PageFooter = defineAsyncComponent(() => import("./components/common/footer/PageFooter.vue"));
const px: string = "23px";
</script>

<template>
  <div class="layout">
    <page-header />
    <page-body />
    <page-footer />
  </div>
</template>

<!-- 界面布局单位 -->
<style lang="scss">
$layout: v-bind(px);
</style>

<style lang="scss">
.layout {
  width: 100%;
  height: 100vh;
  display: grid;
  grid-template-rows: 30px calc(100vh - 110px) 80px;
  grid-template-columns: 1fr;
}
</style>
