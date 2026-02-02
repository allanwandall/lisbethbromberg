<template>
  <h2 class="offer-header">Jeg tilbyder følgende ydelser:</h2>
  <section>
    <div class="text-container light">
      <h2>Familiebehandling (§30 og §32)</h2>
      <p>{{ familieText }}</p>
    </div>
  </section>
  <section>
    <div class="text-container lighter">
      <h2>
        Støtteperson til forældre, hvis barn er anbragt udenfor hjemmet (§ 75)
      </h2>
      <p>{{ stoetteText }}</p>
    </div>
  </section>
  <section>
    <div class="text-container light">
      <h2>Støtte til samvær</h2>
      <p>{{ samvaerText }}</p>
    </div>
  </section>
  <section>
    <div class="text-container lighter">
      <h2>Terapi til børn og unge</h2>
      <p>{{ boernText }}</p>
    </div>
  </section>
  <button @click="goToContact">KONTAKT</button>
</template>

<script setup>
import familieText from "@/content/familiebehandling.txt?raw";
import samvaerText from "@/content/samvaer.txt?raw";
import stoetteText from "@/content/stoetteperson.txt?raw";
import boernText from "@/content/boern_kommune.txt?raw";
import { store } from "@/stores/store";

function goToContact() {
  store.site = "contact";
  window.scrollTo({
    top: 0,
    behavior: "smooth",
  });
}
</script>

<style scoped>
.text-container {
  padding: 5rem;
}

section {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: stretch;
  gap: var(--gap-size);
}

.offer-header {
  margin-left: calc(var(--gap-size) + 5rem);
  margin-top: 2rem;
  font-size: 1.5em;
}

button {
  align-self: center;
  width: 200px;
}

@media (max-width: 1200px) {
  .text-container {
    padding: 2rem;
  }

  .offer-header {
    margin-left: calc(var(--gap-size) + 2rem);
  }
}
</style>
