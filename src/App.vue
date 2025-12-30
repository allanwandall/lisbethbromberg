<template>
  <div class="main-container">
    <NavBar :class="{ scrolled: isScrolled }"></NavBar>
    <div class="main-content">
      <h1>Denne side er under konstruktion</h1>
      <h3>Kontakt Lisbeth på lisbethbromberg@protonmail.com eller 93 80 99 82</h3>
    </div>
  </div>
</template>

<script setup>
import NavBar from './components/NavBar.vue'
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
  align-items: center;
  gap: 1rem;
}

.main-content h1 {
  font-size: 2rem;
} 

.main-content h3 {
  font-size: 1rem;
  font-weight: lighter;
}


.big-content {
  width: 100px;
  height: 120vh;
}

</style>
