<script setup>
import BaseIcons from '../BaseIcons.vue'
import SidebarMarker from '../sidebar-marker/SidebarMarker.vue'

defineProps({
  icon: String,
  type: String,
  title: String,
  taskStatus: Boolean,
})
</script>

<style scoped src="./SidebarTask.less"></style>

<template>
  <div class="sidebar-task">
    <div class="sidebar-task__content">
      <div class="sidebar-task__title">
        <a href="#">
          <BaseIcons name="sidebar-roadmap" v-if="icon === 'roadmap'" />
          <BaseIcons name="sidebar-glossary" v-else-if="icon === 'glossary'" />
          <BaseIcons name="sidebar-exercise" v-else-if="icon === 'exercise'" />
          <BaseIcons name="sidebar-folder" v-else-if="icon === 'folder'" />
          <BaseIcons name="sidebar-file" v-else-if="icon === 'file'" />
        </a>

        <a href="#">
          <p class="sidebar-task__text">{{ title }}</p>
        </a>
      </div>

      <div class="course-task__type">
        <SidebarMarker v-if="type === 'marker'" />
      </div>
    </div>
  </div>
</template>
