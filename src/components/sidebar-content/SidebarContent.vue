<script setup>
import { ref } from 'vue'
import BaseIcons from '../BaseIcons.vue'
import SidebarModule from '../sidebar-module/SidebarModule.vue'
import SidebarTask from '../sidebar-task/SidebarTask.vue'

const isClicked = ref(true)
const clickButton = () => {
  isClicked.value = !isClicked.value
}
</script>

<style scoped src="./SidebarContent.less"></style>

<template>
  <div class="sidebar-content">
    <div class="sidebar-content__title" @click="clickButton">
      <div class="sidebar-content__title-text">
        <BaseIcons name="content" />
        <p>Содержание</p>
      </div>
      <div class="sidebar-content__title-icon">
        <BaseIcons name="arrow-down" v-if="isClicked" />
        <BaseIcons name="arrow-right" v-else-if="!isClicked" />
      </div>
    </div>

    <section class="sidebar-content__modules">
      <SidebarModule label="Общее" v-if="isClicked">
        <div class="sidebar-content__content">
          <ul class="sidebar-content__content-list">
            <li class="sidebar-content__content-item">
              <SidebarTask icon="roadmap" type="marker" title="Список литературы по модулю" />
            </li>
            <li class="sidebar-content__content-item">
              <SidebarTask icon="glossary" type="marker" title="Глоссарий" />
            </li>
            <li class="sidebar-content__content-item">
              <SidebarTask icon="exercise" type="marker" title="Задание" />
            </li>
            <li class="sidebar-content__content-item">
              <SidebarTask icon="folder" type="marker" title="Дополнительная литература" />
            </li>
            <li class="sidebar-content__content-item">
              <SidebarTask icon="file" type="marker" title="Файл" />
            </li>
          </ul>
        </div>
      </SidebarModule>

      <SidebarModule
        label="Модуль 1. Объекты интеллектуальной собственности. Интеллектуальные права. Правовая охрана объектов"
        v-if="isClicked"
      >
        <div class="sidebar-content__content">
          <ul class="sidebar-content__content-list">
            <li class="sidebar-content__content-item">
              <SidebarTask icon="roadmap" type="marker" title="Лекция" />
            </li>
            <li class="sidebar-content__content-item">
              <SidebarTask icon="glossary" type="marker" title="Глоссарий" />
            </li>
            <li class="sidebar-content__content-item">
              <SidebarTask icon="exercise" type="marker" title="Задание" />
            </li>
            <li class="sidebar-content__content-item">
              <SidebarTask icon="file" type="marker" title="Список литературы по модулю" />
            </li>
          </ul>
        </div>
      </SidebarModule>

      <SidebarModule label="Модуль 2. Модели разработки программного продукта" v-if="isClicked">
        <div class="sidebar-content__content">
          <ul class="sidebar-content__content-list">
            <li class="sidebar-content__content-item">
              <SidebarTask icon="roadmap" type="marker" title="Лекция" />
            </li>
            <li class="sidebar-content__content-item">
              <SidebarTask icon="glossary" type="marker" title="Глоссарий" />
            </li>
            <li class="sidebar-content__content-item">
              <SidebarTask icon="exercise" type="marker" title="Задание" />
            </li>
            <li class="sidebar-content__content-item">
              <SidebarTask icon="file" type="marker" title="Список литературы по модулю" />
            </li>
          </ul>
        </div>
      </SidebarModule>
    </section>
  </div>
</template>
