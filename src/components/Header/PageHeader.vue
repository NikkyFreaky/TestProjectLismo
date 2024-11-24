<script setup>
import style from './PageHeader.module.less'
import BaseIcons from '../BaseIcons.vue'
</script>

<template>
  <header :class="style.header">
    <div :class="style.header__logo">
      <a href="#" :class="style.header__logo_link">
        <BaseIcons name="tusur-logo" :class="style.header__logo_img" />
      </a>
    </div>

    <div :class="style.header__main">
      <div :class="style.header__control">
        <a href="#">
          <BaseIcons name="notification" :class="style.header__icon" />
        </a>
        <a href="#">
          <BaseIcons name="chat" :class="style.header__icon" />
        </a>
        <a href="#">
          <BaseIcons name="calendar" :class="style.header__icon" />
        </a>
      </div>

      <div :class="style.header__profile">
        <div :class="style.header__user">
          <a href="#">
            <BaseIcons name="user-profile-avatar" :class="style.header__avatar" />
          </a>
          <a href="#" :class="style.header__user_name">Иван Иванов</a>
        </div>

        <button :class="style.header__logout">Выход</button>
      </div>
    </div>
  </header>
</template>
