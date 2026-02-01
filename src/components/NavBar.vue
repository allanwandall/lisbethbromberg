<template>
  <header class="navbar-container" :class="{ scrolled: isScrolled }">
    <div class="navbar-section">
      <img src="@/assets/lisbergbrombethlogo.png" alt="Logo" class="logo" />
      <div class="title-container">
        <h1>Lisbeth Bromberg</h1>
        <h2>Psykoterapeut MPF</h2>
      </div>
    </div>
    <div class="navbar-section page-selectors">
      <h2 class="page-selector" @click="() => handleClick('landing')">
        Forside
      </h2>
      <h2 class="page-selector" @click="() => handleClick('about')">Om mig</h2>
      <h2 class="page-selector" @click="() => handleClick('therapy')">
        Terapi
      </h2>
      <h2 class="page-selector" @click="() => handleClick('public')">
        Til kommuner
      </h2>

      <h2 class="page-selector" @click="() => handleClick('price')">Priser</h2>
      <h2 class="page-selector" @click="() => handleClick('contact')">
        Kontakt
      </h2>
    </div>
    <div class="burger-menu" @click="toggleBurger">
      <img src="@/assets/burger-menu.png" alt="Logo" class="logo" />
      <div class="burger-context" v-if="burgerOpen">
        <ul>
          <li @click="() => handleClick('landing')">Forside</li>
          <li @click="() => handleClick('about')">Om mig</li>
          <li @click="() => handleClick('therapy')">Terapi</li>
          <li @click="() => handleClick('public')">Til kommuner</li>
          <li @click="() => handleClick('price')">Priser</li>
          <li @click="() => handleClick('contact')">Kontakt</li>
        </ul>
      </div>
    </div>
  </header>
</template>

<script setup>
import { store } from "@/stores/store";
import { ref, onMounted, onUnmounted } from "vue";

const isScrolled = ref(false);
const burgerOpen = ref(false);

function toggleBurger() {
  burgerOpen.value = !burgerOpen.value;
}

function handleScroll() {
  isScrolled.value = window.scrollY > 0;
}

onMounted(() => {
  window.addEventListener("scroll", handleScroll);
});

onUnmounted(() => {
  window.removeEventListener("scroll", handleScroll);
});

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
  font-family: "Lora", serif;
  gap: 2rem;
  z-index: 1000;
  transition:
    box-shadow 0.2s ease-in-out,
    background-color 0.2s ease-in-out;
  -webkit-user-select: none; /* Safari */
  -moz-user-select: none; /* Firefox */
  -ms-user-select: none; /* IE10+ */
  user-select: none; /* Standard */
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

.title-container {
  position: relative;
  display: inline-block;
  padding-right: 40px;
}

.page-selector {
  text-decoration: none;
  cursor: pointer;
  transition:
    color 0.1s ease-in-out,
    text-decoration 0.1s ease-in-out;
}

.page-selector:hover {
  color: #f39c12;
  text-decoration: underline;
}

.scrolled {
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.2);
}

.title-container {
  display: flex;
  flex-direction: row;
  justify-content: flex-start;
  align-items: flex-end;
  gap: 20px;
}

.burger-menu {
  display: none;
}

@media (max-width: 768px) {
  .title-container {
    flex-direction: column;
    justify-content: center;
    align-items: flex-start;
    gap: 0;
    font-size: 0.7em;
  }

  .page-selectors {
    display: none;
  }

  .logo {
    height: 50px;
  }

  .burger-menu {
    border-radius: 50%;
    height: 50px;
    width: 50px;
    display: flex;
    justify-content: center;
    align-items: center;
    background-color: var(--farve-logo);
    position: relative;
  }

  .burger-menu img {
    height: 40%;
    width: 40%;
    overflow: visible;
    object-fit: contain;
  }

  .burger-context {
    position: absolute;
    top: 60px;
    right: -10px;
    background-color: var(--farve-logo);
    color: white;
    border-radius: 15px;
    padding: 13px;
    width: 200px;
  }

  .burger-context li {
    font-size: 2em;
    z-index: 2;
  }

  .burger-context ul {
    list-style-type: none;
    padding: 0;
    margin: 0;
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    justify-content: flex-start;
    gap: 15px;
  }
}
</style>
