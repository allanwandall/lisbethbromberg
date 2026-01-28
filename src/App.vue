<template>
  <div class="main-container">
    <NavBar></NavBar>
    <div class="main-content">
      <LandingPage v-if="store.site === 'landing'"></LandingPage>
    </div>
    <div class="footer-container">
      <hr>
      <img src="@/assets/lisbergbrombethlogo.png" alt="Logo" class="logo" />
      <hr>
    </div>
  </div>
</template>

<script setup>
import NavBar from './components/NavBar.vue'
import LandingPage from './components/LandingPage.vue'
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
  margin-top: 70px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: stretch;
  gap: 3rem;
  margin-bottom: 3rem;
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

hr {
  border: none;
  height: 1px;
  background-color: #E0E0E0;
  width: 30%;
  margin: 0;
}

</style>
