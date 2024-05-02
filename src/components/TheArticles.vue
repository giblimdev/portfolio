<script setup>
import { ref } from 'vue'
import { articles } from '../stores/ArticlesArray.js'
import Modal from './modal.vue'

const showModal = ref(false)
const currentArticle = ref({})

const openModal = (article) => {
  currentArticle.value = article
  showModal.value = true
}

const closeModal = () => {
  showModal.value = false
}
</script>

<template>
  <div class="thearticles">
    <h1>Liste des Articless</h1>
    <!-- <div cassName="container-fluid d-flex flex-wrap justify-content-center">-->
    <div class="article-container">
      <div v-for="article in articles" :key="article.id" @click="openModal(article)">
        <div class="article-list">
          <div class="articleimage">
            <img class="img" v-bind:src="'/src/assets/img/' + article.image" />
          </div>
          <h2>{{ article.name }}</h2>
        </div>
      </div>
    </div>
  </div>
  <!-- Modal Component -->
  <Modal v-if="showModal" :article="currentArticle" @close="closeModal" />
</template>

<style scoped>
.thearticles {
  height: 70vh;
}
.article-container {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  padding: 20px;
}

.article-list {
  width: 100px;
  height: 140px;
  border-radius: 20px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.8);
  padding: 1rem;
  margin: 5px;
  padding: 10px;
  border: 1px solid #17eb3e;
  cursor: pointer;
  overflow: hidden;
}
.article-list:hover {
  transform: scale(1.1);
}
.articleimage {
  border: solid;
  overflow: hidden;
  padding: 5px;
  max-width: 200px;
  max-height: 130px;
}
img {
  width: 100%;
  height: auto;
}
h2 {
  font-size: 0.8rem;
}
</style>
