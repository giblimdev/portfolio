<script setup>
import { defineProps, defineEmits } from 'vue'

const props = defineProps({
  article: Object
})

const emit = defineEmits(['close'])

const closeModal = () => {
  emit('close')
}
</script>
<template>
  <div class="modal-overlay" @click.self="closeModal">
    <div class="modal-content">
      <div class="articleimage">
        <img class="img" v-bind:src="'/src/assets/img/' + article.image" />
      </div>

      <h2>{{ article.name }}</h2>
      <p>{{ article.technology }}</p>
      <button class="btnmodal">
        <a v-bind:href="article.lien" target="_blank">Découvrir</a>
      </button>

      <p>{{ article.date }}</p>
      <button @click="closeModal">Fermer</button>
    </div>
  </div>
</template>
<style scoped>
.modal-overlay {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;

  background-color: rgba(0, 0, 0, 0.6);
  display: flex;
  justify-content: center;
  align-items: center;
}

.modal-content {
  width: 50%;
  height: 90vh;
  border: solid red;
  background: white;
  padding: 2rem;
  border-radius: 10px;
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
.btnmodal {
  background-color: blue;
  border-radius: 10px;
}
a:hover {
  font-weight: bold;
  transform: scale(1.1);
  font-size: 1.1rem;
}
</style>
