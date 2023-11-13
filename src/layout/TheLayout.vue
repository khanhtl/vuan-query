<template>
    <a-layout class="the-layout">
        <the-sidebar :collapsed="collapsed"></the-sidebar>
        <a-layout class="main-content">
            <the-header :collapsed="collapsed" @collapsed-change="collapsed = $event"></the-header>
            <a-layout-content class="content-container" :style="{ margin: '24px 16px', padding: '24px', background: '#fff', minHeight: '280px' }">
                Content
            </a-layout-content>
        </a-layout>
    </a-layout>
</template>
<script setup lang="ts">
import TheHeader from './TheHeader.vue';
import TheSidebar from './TheSidebar.vue';
import {ref} from 'vue'
const collapsed = ref(true);

</script>
<style lang="scss" scoped>
.the-layout {
    width: 100vw;
    height: 100vh;
    overflow: hidden;
}
#components-layout-demo-custom-trigger .trigger {
  font-size: 18px;
  line-height: 64px;
  padding: 0 24px;
  cursor: pointer;
  transition: color 0.3s;
}

#components-layout-demo-custom-trigger .trigger:hover {
  color: #1890ff;
}

#components-layout-demo-custom-trigger .logo {
  height: 32px;
  background: rgba(255, 255, 255, 0.3);
  margin: 16px;
}

.site-layout .site-layout-background {
  background: #fff;
}
</style>