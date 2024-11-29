<script setup>
import BaseIcons from '../BaseIcons.vue'

defineProps({
  condition: {
    type: Array,
    required: true,
    default: () => [
      { text: 'Получить оценку', done: false },
      { text: 'Просмотреть', done: true },
      { text: 'Получить оценку', done: true },
    ],
  },
})
</script>

<style scoped src="./CourseCondition.less"></style>

<template>
  <div class="course-condition">
    <div
      v-for="item in condition"
      :key="item.text"
      class="course-condition__item"
      :class="{
        'course-condition__done': item.done,
        'course-condition__must-do': !item.done,
      }"
    >
      <div v-if="item.done" class="course-condition__done">
        <BaseIcons name="task-done" class="course-condition__icon" />
        <span class="course-condition__text">Выполнено:</span>
        {{ item.text }}
      </div>
      <div v-else class="course-condition__must-do">
        <span class="course-condition__text">Надо сделать:</span>
        {{ item.text }}
      </div>
    </div>
  </div>
</template>
