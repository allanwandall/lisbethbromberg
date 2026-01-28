<template>
  <header class="navbar-container" :class="{ scrolled: isScrolled }">
    <div class="navbar-section">
      <img src="@/assets/lisbergbrombethlogo.png" alt="Logo" class="logo" />
      <h1>Lisbeth Bromberg</h1>
      <h2>Psykoterapeut</h2>
    </div>
    <div class="navbar-section">
      <h2 class="page-selector" @click="() => handleClick('landing')">
        Forside
      </h2>
      <h2 class="page-selector" @click="() => handleClick('about')">Om mig</h2>
      <h2 class="page-selector" @click="() => handleClick('therapy')">Terapi</h2>
      <h2 class="page-selector" @click="() => handleClick('public')">Til kommuner</h2>
      
      <h2 class="page-selector" @click="() => handleClick('price')">
        Priser
      </h2>
      <h2 class="page-selector" @click="() => handleClick('contact')">
        Kontakt
      </h2>
    </div>
  </header>
</template>

<script setup>
import { store } from "@/stores/store";
import { ref, onMounted, onUnmounted } from 'vue'

const isScrolled = ref(false)

function handleScroll() {
  isScrolled.value = window.scrollY > 0
}

onMounted(() => {
  window.addEventListener('scroll', handleScroll)
})

onUnmounted(() => {
  window.removeEventListener('scroll', handleScroll)
})
  

function handleClick(page) {
  store.site = page;
}
</script>

<style scoped>
.navbar-container {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 90px;
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: space-between;
  padding: 1rem 2rem;
  background-color: var(--bg-color);
  font-family: 'Lora', serif;
  gap: 2rem;
  z-index: 1000;
  transition: box-shadow 0.2s ease-in-out, background-color 0.2s ease-in-out;
  -webkit-user-select: none; /* Safari */
  -moz-user-select: none;    /* Firefox */
  -ms-user-select: none;     /* IE10+ */
  user-select: none;         /* Standard */
}

.logo {
  height: 60px;
  width: auto;
}

h1 {
  margin: 0;
  font-size: 2em;
  font-weight: bold;
  letter-spacing: 0.02em;
  cursor: default;
}

h2 {
  color: black;
  font-weight: lighter;
  font-size: 1.2em;
}

.navbar-section {
  display: flex;
  gap: 1rem;
  align-items: center;
  justify-content: space-between;
}

.page-selector {
  text-decoration: none;
  cursor: pointer;
  transition: color 0.1s ease-in-out, text-decoration 0.1s ease-in-out;
}

.page-selector:hover {
  color: #f39c12;
  text-decoration: underline;
}

.scrolled {
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.2);
}
</style>
