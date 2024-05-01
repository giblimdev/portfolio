<script setup>
/*defineProps({
  date: {
    type: String,
    required: true
  }
})*/
</script>
<template>
  <!--<div><h1 class="green">{{ msg }}</h1></div>-->
  <header id="header">
    <a href="#header">
      <img alt="Vue logo" class="sol" src="@/assets/img/logo.png" width="75" height="75"
    /></a>
    <h1 class="sol foldit">TechnoCloudSolution</h1>
    <nav class="contener">
      <div class="link">
        <RouterLink to="/">Home</RouterLink>
      </div>
      <div class="link">
        <RouterLink to="/about">About</RouterLink>
      </div>
    </nav>
  </header>
</template>
<style scoped>
header {
  background: linear-gradient(135deg, #427783 0%, #03657e 100%);
  color: white;
  border-radius: 0px 0px 20px 20px;
  display: flex;
  justify-content: space-around;
  align-items: center;
  height: 15vh;
  width: 100%;
  position: fixed;
  top: 0;
  left: 0;
}
.link {
  margin: 10px;
}
</style>
