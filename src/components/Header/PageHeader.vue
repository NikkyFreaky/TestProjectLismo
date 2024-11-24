<script setup>
import style from './PageHeader.module.less'
</script>

<template>
  <header :class="style.header">
    <div :class="style.header__logo">
      <a href="#" :class="style.header__logo_link">
        <img
          src="@/assets/svg-sprite/tusur-logo.svg"
          alt="tusur-logo"
          :class="style.header__logo_img"
        />
      </a>
    </div>

    <div :class="style.header__main">
      <div :class="style.header__control">
        <a href="#">
          <img
            src="@/assets/svg-sprite/notification.svg"
            alt="notification"
            :class="style.header__icon"
          />
        </a>
        <a href="#">
          <img src="@/assets/svg-sprite/chat.svg" alt="chat" :class="style.header__icon" />
        </a>
        <a href="#">
          <img src="@/assets/svg-sprite/calendar.svg" alt="calendar" :class="style.header__icon" />
        </a>
      </div>

      <div :class="style.header__profile">
        <div :class="style.header__user">
          <img
            src="@/assets/svg-sprite/user-profile-icon.svg"
            alt="profile-icon"
            :class="style.header__avatar"
          />
          <a href="#" :class="style.header__user_name">Иван Иванов</a>
        </div>

        <button :class="style.header__logout">Выход</button>
      </div>
    </div>
  </header>
</template>
