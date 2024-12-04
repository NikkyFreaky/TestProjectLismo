<script setup>
import BaseIcons from '../BaseIcons.vue'
import Button from '../buttons/BaseButtons.vue'
import SidebarContent from '../sidebar-content/SidebarContent.vue'

import { sidebarVisibility } from '@/stores/sideBar.js'
</script>

<style scoped src="./PageSidebar.less"></style>

<template>
  <aside :class="['page-sidebar', sidebarVisibility ? 'page-sidebar__active' : '']">
    <Button type="back" class="page-sidebar__button" />
    <nav class="page-sidebar__content">
      <ul>
        <li>
          <SidebarContent />
        </li>
        <li>
          <a href="#" class="page-sidebar__item"> <BaseIcons name="people" />Участники </a>
        </li>
        <li>
          <a href="#" class="page-sidebar__item"> <BaseIcons name="grade" />Оценки </a>
        </li>
      </ul>
    </nav>
  </aside>
</template>
