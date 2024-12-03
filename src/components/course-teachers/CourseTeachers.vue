<script setup>
import AdditionalTeachers from '../course-additional-teachers/AdditionalTeachers.vue'
</script>

<style scoped src="./CourseTeachers.less"></style>

<template>
  <div class="course-teachers">
    <h2 class="course-teachers__title">Преподаватели курса:</h2>
    <ul class="course-teachers__list">
      <li class="course-teachers__item">
        <img
          src="@/assets/images/course/teachers/demakova.png"
          alt="teacher"
          class="course-teachers__image"
        />
        <span class="course-teachers__name">А. В. Демакова</span>
      </li>
      <li class="course-teachers__item">
        <img
          src="@/assets/images/course/teachers/kvasnikova.png"
          alt="teacher"
          class="course-teachers__image"
        />
        <span class="course-teachers__name">А. А. Квасникова</span>
      </li>
      <li class="course-teachers__item">
        <img
          src="@/assets/images/course/teachers/krasina.png"
          alt="teacher"
          class="course-teachers__image"
        />
        <span class="course-teachers__name">А. А. Красина</span>
      </li>
      <li class="course-teachers__item">
        <AdditionalTeachers />
      </li>
    </ul>
  </div>
</template>
