<script setup>
import BaseIcons from '../BaseIcons.vue'
import Button from '../buttons/BaseButtons.vue'
import Content from '../sidebar-content/SidebarContent.vue'
</script>

<style scoped src="./PageSidebar.less"></style>

<template>
  <aside class="page-sidebar">
    <Button type="back" />
    <nav>
      <ul>
        <li>
          <Content />
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
