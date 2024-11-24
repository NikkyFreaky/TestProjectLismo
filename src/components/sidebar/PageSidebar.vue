<script setup>
import style from './PageSidebar.module.less'
import BaseButtons from '../buttons/BaseButtons.vue'
import BaseIcons from '../BaseIcons.vue'
</script>

<template>
  <aside :class="style.sidebar">
    <BaseButtons type="back" />
    <nav>
      <ul>
        <li>
          <a href="#" :class="style.sidebar__item"> <BaseIcons name="people" />Участники </a>
        </li>
        <li>
          <a href="#" :class="style.sidebar__item"> <BaseIcons name="grade" />Оценки </a>
        </li>
      </ul>
    </nav>
  </aside>
</template>
