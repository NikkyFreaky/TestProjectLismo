<script setup>
import style from './BaseButtons.module.less'
import BaseIcons from '../BaseIcons.vue'
</script>

<template>
  <button :class="style.button">
    <a href="#" :class="style.button__back">
      <BaseIcons name="arrow-back" />Назад к списку курсов
    </a>
  </button>
</template>
