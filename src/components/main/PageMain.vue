<script setup>
import CourseDescription from '../course-description/CourseDescription.vue'
import CourseTeachers from '../course-teachers/CourseTeachers.vue'
import CourseProgressBar from '../course-progress-bar/CourseProgressBar.vue'
import CourseContent from '../course-content/CourseContent.vue'
import CourseTask from '../course-task/CourseTask.vue'
import PageFooter from '../footer/PageFooter.vue'
</script>

<style scoped src="./PageMain.less"></style>

<template>
  <main class="page-main">
    <div class="page-main__background"></div>
    <div class="page-main__wrapper">
      <div class="page-main__content">
        <section class="page-main__course-description">
          <CourseDescription />
          <CourseTeachers />
        </section>

        <section class="page-main__course-progress-bar">
          <CourseProgressBar />
        </section>

        <CourseContent label="Общее" closeAll>
          <div class="page-main__course-content">
            <p class="page-main__course-content-description">Материалы для изучения</p>
            <ul class="page-main__course-content-list">
              <li class="page-main__course-content-item">
                <CourseTask icon="roadmap" type="condition" title="Список литературы по модулю" />
              </li>
              <li class="page-main__course-content-item">
                <CourseTask icon="glossary" type="button" title="Глоссарий" />
              </li>
              <li class="page-main__course-content-item">
                <CourseTask icon="exercise" type="condition-multiple" title="Задание" />
              </li>
              <li class="page-main__course-content-item">
                <CourseTask icon="folder" type="button" closed title="Дополнительная литература" />
              </li>
              <li class="page-main__course-content-item">
                <CourseTask icon="file" type="button" title="Файл" />
              </li>
            </ul>
          </div>
        </CourseContent>

        <CourseContent
          label="Модуль 1. Объекты интеллектуальной собственности. Интеллектуальные права. Правовая охрана объектов"
        >
          <div class="page-main__course-content">
            <ul class="page-main__course-content-list">
              <li class="page-main__course-content-item">
                <CourseTask icon="roadmap" type="condition" title="Лекция" />
              </li>
              <li class="page-main__course-content-item">
                <CourseTask icon="glossary" type="button" title="Глоссарий" />
              </li>
              <li class="page-main__course-content-item">
                <CourseTask icon="exercise" type="condition-multiple" title="Задание" />
              </li>
              <li class="page-main__course-content-item">
                <CourseTask icon="file" type="button" title="Список литературы по модулю" />
              </li>
            </ul>
          </div>
        </CourseContent>

        <CourseContent label="Модуль 2. Модели разработки программного продукта">
          <div class="page-main__course-content">
            <ul class="page-main__course-content-list">
              <li class="page-main__course-content-item">
                <CourseTask icon="roadmap" type="condition" title="Лекция" />
              </li>
              <li class="page-main__course-content-item">
                <CourseTask icon="glossary" type="button" title="Глоссарий" />
              </li>
              <li class="page-main__course-content-item">
                <CourseTask icon="exercise" type="condition-multiple" title="Задание" />
              </li>
              <li class="page-main__course-content-item">
                <CourseTask icon="file" type="button" title="Список литературы по модулю" />
              </li>
            </ul>
          </div>
        </CourseContent>
      </div>
    </div>
  </main>
  <PageFooter />
</template>
