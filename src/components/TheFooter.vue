<script setup>
//import { LastMAJ } from '../stores/DateMAJ.js'
//const LastMAJ = setLastMAJ()
const LastMAJ = '21-04-2024'
</script>

<template>
  <footer class="contener">
    <div>
      <p class="">Dernière mise a jour : {{ LastMAJ }}</p>
    </div>
    <div class="box_logo">
      <a class="a_logo" href="https://linkedin.com/in/" target="_blank">
        <img src="@/assets/img/linkedin.png" alt="Logo LinkedIn" />
      </a>
      <a class="a_logo" href="https://github.com/" target="_blank"
        ><img src="@/assets/img/github.png" alt="Logo GitHub"
      /></a>
    </div>
  </footer>
</template>
<style scoped>
footer {
  background: linear-gradient(135deg, #427783 0%, #03657e 100%);
  border-radius: 20px 20px 0px 0px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  height: 10vh;
  width: 100%;
  position: fixed;
  bottom: 0px;
  left: -0px;
  padding: 10px;
}
.box_logo {
  border: solid red;
  display: flex;
  justify-content: space-around;
  margin: 5px auto;
  padding: 2px;
  border-radius: 10px;
  background-color: rgb(39, 39, 40);
}
.a_logo {
  margin: 5px;
}
img {
  height: 20px;
  width: 20px;
}
</style>
