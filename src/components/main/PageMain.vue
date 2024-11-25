<script setup>
import CourseInfo from '../course-description/CourseDescription.vue'
import CourseTeachers from '../course-teachers/CourseTeachers.vue'
import CourseProgressBar from '../course-progress-bar/CourseProgressBar.vue'
import PageFooter from '../footer/PageFooter.vue'
</script>

<style scoped src="./PageMain.less"></style>

<template>
  <main class="page-main">
    <div class="page-main__background"></div>
    <div class="page-main__wrapper">
      <div class="page-main__content">
        <section class="page-main__course-description">
          <CourseInfo />
          <CourseTeachers />
        </section>

        <section class="page-main__course-progress-bar">
          <CourseProgressBar />
        </section>
      </div>
    </div>
  </main>
  <PageFooter />
</template>
