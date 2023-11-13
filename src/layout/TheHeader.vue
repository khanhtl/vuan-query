<template>
    <a-layout-header class="the-header" style="background: #fff; padding: 0">
        <menu-unfold-outlined v-if="collapsed" class="trigger" @click="emit('collapsedChange', false)" />
        <menu-fold-outlined v-else class="trigger" @click="emit('collapsedChange', true)" />
    </a-layout-header>
</template>
<script setup lang="ts">
import {
    MenuUnfoldOutlined,
    MenuFoldOutlined,
} from '@ant-design/icons-vue';
const emit = defineEmits(['collapsedChange'])
const props = defineProps<{
    collapsed: boolean
}>();
</script>
<style lang="scss"></style>