<script setup>
import BaseButtons from '../buttons/BaseButtons.vue'
import BaseIcons from '../BaseIcons.vue'
</script>

<style scoped src="./PageSidebar.less"></style>

<template>
  <aside class="page-sidebar">
    <BaseButtons type="back" />
    <nav>
      <ul>
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
