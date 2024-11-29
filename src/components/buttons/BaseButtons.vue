<script setup>
import { ref } from 'vue'
import BaseIcons from '../BaseIcons.vue'

const buttonType = ref(false)

function buttonChange() {
  buttonType.value = !buttonType.value
}

defineProps({
  type: String,
})
</script>

<style scoped src="./BaseButtons.less"></style>

<template>
  <button class="base-button" v-if="type === 'back'">
    <span class="base-button__back">
      <BaseIcons name="arrow-back" />
      <span>Назад к списку курсов</span>
    </span>
  </button>

  <div v-else-if="type === 'mark'">
    <button
      class="base-button"
      :class="{ 'base-button__mark': !buttonType, 'base-button__mark-done': buttonType }"
      @click="buttonChange"
    >
      <span v-if="buttonType" class="base-button__mark-done">
        <BaseIcons name="task-done" />
        <span>Выполнено</span>
      </span>
      <span v-else class="base-button__mark">
        <span>Отметить как выполненный</span>
      </span>
    </button>
  </div>
</template>
