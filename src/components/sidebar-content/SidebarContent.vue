<script setup>
import { ref } from 'vue'
import BaseIcons from '../BaseIcons.vue'

const isClicked = ref(true)
const clickButton = () => {
  isClicked.value = !isClicked.value
}
</script>

<style scoped src="./SidebarContent.less"></style>

<template>
  <div class="sidebar-content" @click="clickButton">
    <div class="sidebar-content__title">
      <BaseIcons name="content" /> Содержание
      <BaseIcons name="arrow-down" v-if="isClicked" />
      <BaseIcons name="arrow-right" v-else-if="!isClicked" />
    </div>
  </div>
</template>
