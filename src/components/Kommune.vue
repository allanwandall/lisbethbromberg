<template>
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
</template>

<script setup>
import familieText from "@/content/familiebehandling.txt?raw";
import samvaerText from "@/content/samvaer.txt?raw";
import stoetteText from "@/content/stoetteperson.txt?raw";
import boernText from "@/content/boern_kommune.txt?raw";
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

@media (max-width: 768px) {
  .text-container {
    padding: 2rem;
  }
}
</style>
