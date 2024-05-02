<script setup></script>
<template>
  <header>
    <RouterLink to="/">
      <img alt="Vue logo" class="" src="@/assets/img/logo.png" width="50" height="50" />
    </RouterLink>

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
h1 {
  font-size: 1.2rem;
}
.link {
  margin: 10px;
}
a:hover {
  font-weight: bold;
  transform: scale(1.1);
  font-size: 1.1rem;
}
</style>
