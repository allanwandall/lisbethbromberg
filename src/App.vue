<template>
  <div class="main-container">
    <NavBar></NavBar>
    <div class="main-content">
      <Forside v-if="store.site === 'landing'"></Forside>
      <About v-if="store.site === 'about'"></About>
      <Kommune v-if="store.site === 'public'"></Kommune>
      <Terapi v-if="store.site === 'therapy'"></Terapi>
      <Priser v-if="store.site === 'price'"></Priser>
    </div>
    <div class="footer-container">
      <img src="@/assets/lisbergbrombethlogo.png" alt="Logo" class="logo" />

    </div>
  </div>
</template>

<script setup>
import NavBar from './components/NavBar.vue'
import Forside from './components/Forside.vue'
import About from './components/About.vue'
import Kommune from './components/Kommune.vue'
import Terapi from './components/Terapi.vue'
import Priser from './components/Priser.vue'
import { store } from "@/stores/store";

</script>

<style scoped>
img {
  width: 300px;
}

.main-container {
  width: 100%;
  flex: 1;
  display: flex;
  flex-direction: column;
  align-items: stretch;
  justify-content: flex-start;
  gap: 2rem;
  position: relative;
  background-color: var(--bg-color);
  transition: box-shadow 0.6s ease-in-out, background-color 0.6s ease-in-out;
}

.main-content {
  margin-top: 90px;
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  align-items: stretch;
  gap: var(--gap-size);
}

.main-content h1 {
  font-size: 2rem;
} 

.main-content h3 {
  font-size: 1rem;
  font-weight: lighter;
}

.footer-container {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: center;
  gap: 5rem;
  width: 100%;
  margin-bottom: 1rem;
}

.logo {
  height: 60px;
  width: auto;
}


</style>
