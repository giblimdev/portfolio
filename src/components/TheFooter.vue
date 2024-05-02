<script setup>
//import { LastMAJ } from '../stores/DateMAJ.js'

// Crée une nouvelle instance de la classe Date
const dateDuJour = new Date()
const jour = dateDuJour.getDate()
const mois = dateDuJour.getMonth() + 1
const annee = dateDuJour.getFullYear()

//console.log(`Date du jour : ${jour}/${mois}/${annee}`)
</script>

<template>
  <footer class="contener">
    <div>
      <p>Dernière mise a jour : {{ jour }}/{{ mois }}/{{ annee }}</p>
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
