<script setup>
import { RouterLink, RouterView } from 'vue-router'

import TheHeader from './components/TheHeader.vue'
import AboutMe from './components/TheAboutMe.vue'
import TheArticles from './components/TheArticles.vue'
import TheForm from './components/TheForm.vue'
import TheFooter from './components/TheFooter.vue'
</script>

<template>
  <div>
    <TheHeader />
  </div>
  <div class="position">
    <RouterView />
  </div>
  <div class="sol about">
    <AboutMe />
  </div>
  <div class="sol"><TheArticles /></div>
  <div class="sol"><TheForm /></div>
  <footer>
    <TheFooter />
  </footer>

  <div class="add"></div>
</template>

<style scoped>
.about {
  margin-top: 130px;
}
main {
  margin-bottom: 200px;
}
.position {
  background-color: white;
  position: absolute;
  top: 100px;
  left: 0;
}
.add {
  margin-top: 10px;
  height: 10vh;
}
</style>
