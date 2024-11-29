<script setup>
import { ref } from 'vue'
import BaseIcons from '../BaseIcons.vue'

const open = ref(true)

function toggleOpen() {
  open.value = !open.value
}

defineProps({
  label: String,
  closeAll: Boolean,
})
</script>

<style scoped src="./CourseContent.less"></style>

<template>
  <section class="course-content">
    <div class="course-content__header">
      <div
        class="course-content__header-toggle"
        :class="{ 'course-content__header-open': open, 'course-content__header-closed': !open }"
        @click="toggleOpen"
      >
        <BaseIcons :name="open ? 'arrow-down' : 'arrow-right'" class="course-content__icon" />
        <h4 class="course-content__title">{{ label }}</h4>
      </div>
      <span v-if="closeAll" @click="toggleOpen" class="course-content__toggle-all"
        >Свернуть всё</span
      >
    </div>
    <slot v-if="open"></slot>
  </section>
</template>
