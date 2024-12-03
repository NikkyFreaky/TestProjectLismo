<script setup>
import BaseIcons from '../BaseIcons.vue'
</script>

<style scoped src="./ClosedTask.less"></style>

<template>
  <div class="closed-task">
    <BaseIcons name="task-closed" class="closed-task__icon" />
    <p>
      Недоступно, пока не выполнено: Элемент курса <br />
      <span class="closed-task__text">Задание</span> должен быть отмечен как выполненный
    </p>
  </div>
</template>
