<script setup>
import BaseIcons from '../BaseIcons.vue'
import { sidebarVisibility } from '@/stores/sidebar.js'

function toggleMenu() {
  sidebarVisibility.value = !sidebarVisibility.value
}
</script>

<style scoped src="./PageHeader.less"></style>

<template>
  <header class="page-header">
    <div :class="['page-header__logo']">
      <a href="#" class="page-header__logo-link">
        <BaseIcons name="tusur-logo" class="page-header__logo-img" />
      </a>
    </div>

    <div class="page-header__main">
      <div class="page-header__control">
        <a href="#" :class="['page-header__burger-menu']" @click="toggleMenu()">
          <BaseIcons name="burger-menu" class="page-header__icon" />
        </a>
        <a href="#">
          <BaseIcons name="notification" class="page-header__icon" />
        </a>
        <a href="#">
          <BaseIcons name="chat" class="page-header__icon" />
        </a>
        <a href="#">
          <BaseIcons name="calendar" class="page-header__icon" />
        </a>
      </div>

      <div class="page-header__profile">
        <div class="page-header__user">
          <a href="#">
            <BaseIcons name="user-profile-avatar" class="page-header__avatar" />
          </a>
          <a href="#" class="page-header__user_name">Иван Иванов</a>
        </div>

        <button class="page-header__logout_button">Выход</button>
      </div>
    </div>
  </header>
</template>
