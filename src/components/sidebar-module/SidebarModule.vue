<script setup>
import { ref } from 'vue'
import BaseIcons from '../BaseIcons.vue'

const open = ref(false)

function toggleOpen() {
  open.value = !open.value
}

defineProps({
  label: String,
})
</script>

<style scoped src="./SidebarModule.less"></style>

<template>
  <section class="sidebar-module">
    <div class="sidebar-module__header">
      <div
        class="sidebar-module__header-toggle"
        :class="{ 'sidebar-module__header-open': open, 'sidebar-module__header-closed': !open }"
        @click="toggleOpen"
      >
        <h4 class="sidebar-module__title">{{ label }}</h4>

        <div class="sidebar-module__icon">
          <BaseIcons :name="open ? 'arrow-down' : 'arrow-right'" />
        </div>
      </div>
    </div>
    <slot v-if="open"></slot>
  </section>
</template>
