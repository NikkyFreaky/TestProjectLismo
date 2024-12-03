<script setup>
import BaseIcons from '../BaseIcons.vue'
import Button from '../buttons/BaseButtons.vue'
import CourseCondition from '../course-condition/CourseCondition.vue'
import ClosedTask from '../closed-task/ClosedTask.vue'

defineProps({
  icon: String,
  type: String,
  title: String,
  closed: Boolean,
})
</script>

<style scoped src="./CourseTask.less"></style>

<template>
  <div class="course-task">
    <div class="course-task__content">
      <div class="course-task__title">
        <a href="#">
          <BaseIcons name="task-roadmap" class="course-task__icon" v-if="icon === 'roadmap'" />
          <BaseIcons
            name="task-glossary"
            class="course-task__icon"
            v-else-if="icon === 'glossary'"
          />
          <BaseIcons
            name="task-exercise"
            class="course-task__icon"
            v-else-if="icon === 'exercise'"
          />
          <BaseIcons name="task-folder" class="course-task__icon" v-else-if="icon === 'folder'" />
          <BaseIcons name="task-file" class="course-task__icon" v-else-if="icon === 'file'" />
        </a>

        <a href="#">
          <p class="course-task__text">{{ title }}</p>
        </a>
      </div>

      <div class="course-task__type">
        <Button type="mark" v-if="type === 'button'" />
        <CourseCondition
          :condition="[{ text: 'Получить оценку', done: false }]"
          v-if="type === 'condition'"
        />
        <CourseCondition
          :condition="[
            { text: 'Получить оценку', done: false },
            { text: 'Просмотреть', done: true },
            { text: 'Получить оценку', done: true },
          ]"
          v-if="type === 'condition-multiple'"
        />
      </div>
    </div>
    <ClosedTask class="course-task__closed" v-if="closed"></ClosedTask>
  </div>
</template>
