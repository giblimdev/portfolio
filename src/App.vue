<script setup>
import { RouterLink, RouterView } from 'vue-router'

import TheHeader from './components/TheHeader.vue'
import AboutMe from './components/TheAboutMe.vue'
import TheArticles from './components/TheArticles.vue'
import TheForm from './components/TheForm.vue'
import TheFooter from './components/TheFooter.vue'
</script>

<template>
  <div class="sol"><TheHeader /></div>
  <div class="sol about">
    <AboutMe />
  </div>
  <div class="sol"><TheArticles /></div>
  <div class="sol"><TheForm /></div>
  <footer>
    <TheFooter />
  </footer>
  <RouterView />
</template>

<style scoped>
.about {
  margin-top: 160px;
}
main {
  margin-bottom: 200px;
}
</style>
