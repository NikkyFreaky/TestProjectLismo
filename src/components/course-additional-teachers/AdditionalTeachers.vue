<script setup>
import { ref, computed, onMounted, onUnmounted } from 'vue'

const open = ref(false)

const teachers = ref([
  { name: 'К. К. Константинович' },
  { name: 'К. К. Константинович' },
  { name: 'К. К. Константинович' },
  { name: 'К. К. Константинович' },
  { name: 'К. К. Константинович' },
  { name: 'К. К. Константинович' },
  { name: 'К. К. Константинович' },
  { name: 'К. К. Константинович' },
  { name: 'К. К. Константинович' },
  { name: 'К. К. Константинович' },
  { name: 'К. К. Константинович' },
  { name: 'К. К. Константинович' },
  { name: 'К. К. Константинович' },
  { name: 'К. К. Константинович' },
  { name: 'К. К. Константинович' },
  { name: 'К. К. Константинович' },
  { name: 'К. К. Константинович' },
  { name: 'К. К. Константинович' },
  { name: 'К. К. Константинович' },
  { name: 'К. К. Константинович' },
])

const count = computed(() => teachers.value.length)

function toggleOpen() {
  open.value = !open.value
}

function handleClickOutside(event) {
  const teachersList = document.querySelector('.additional-teachers__list')
  if (
    teachersList &&
    !teachersList.contains(event.target) &&
    !event.target.closest('.additional-teachers__toggle')
  ) {
    open.value = false
  }
}

onMounted(() => {
  document.addEventListener('click', handleClickOutside)
})

onUnmounted(() => {
  document.removeEventListener('click', handleClickOutside)
})
</script>

<style scoped src="./AdditionalTeachers.less"></style>

<template>
  <div class="additional-teachers">
    <button class="additional-teachers__toggle" @click="toggleOpen">(ещё +{{ count }})</button>
    <ul v-if="open" class="additional-teachers__list">
      <li v-for="(teacher, index) in teachers" :key="index" class="additional-teachers__item">
        <img
          src="@/assets/images/course/teachers/konstantinovich.png"
          :alt="teacher.name"
          class="additional-teachers__image"
        />
        <span class="additional-teachers__name">{{ teacher.name }}</span>
      </li>
    </ul>
  </div>
</template>
