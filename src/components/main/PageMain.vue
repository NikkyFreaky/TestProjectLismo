<script setup>
import CourseInfo from '../course-description/CourseDescription.vue'
import CourseTeachers from '../course-teachers/CourseTeachers.vue'
import PageFooter from '../footer/PageFooter.vue'
</script>

<style scoped src="./PageMain.less"></style>

<template>
  <main class="page-main">
    <div class="page-main__background"></div>
    <div class="page-main__wrapper">
      <div class="page-main__content">
        <section class="page-main__header">
          <CourseInfo />
          <CourseTeachers />
        </section>
      </div>
    </div>
  </main>
  <PageFooter />
</template>
