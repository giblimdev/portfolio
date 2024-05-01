<script setup>
import { RouterLink, RouterView } from 'vue-router'
</script>
<template>
  <div class="notfound">
    <h1 class="roboto-black">404</h1>
    <div>
      <img alt="img 404" src="../assets/img/404.png" />
    </div>
    <button class="btn_notfound">
      <RouterLink to="/">ACCUEIL</RouterLink>
    </button>
  </div>
</template>

<style scoped>
h1 {
  font-size: 1.5 rem;
}
.notfound {
  background-color: white;
  width: 100%;
  height: 100vh;
  position: fixed;
  top: 0;
  left: 0;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  text-align: center;
  transition: transform 0.3s;
}

img {
  max-width: 80%;
  height: auto;
}

.btn_notfound {
  margin-top: 1rem;
  padding: 10px 20px;
  border-radius: 20px;
  background-color: #007bff;
  color: white;
  font-size: 1.2em;
  border: none;
  cursor: pointer;
  text-decoration: none;
}

.btn_notfound:hover {
  background-color: #0056b3;
  transform: scale(1.05);
}

a {
  color: white;
}
</style>
