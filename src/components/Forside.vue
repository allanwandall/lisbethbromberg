<template>
  <section class="header-mobile">
    <div class="text-container header light">
      <h1>Psykoterapi & familiebehandling</h1>
      <h2>Nærvær, tryghed og forandring</h2>
    </div>
  </section>
  <section class="landing-section">
    <div class="image-container">
      <img
        src="@/assets/Lisbeth.webp"
        alt="Billede af Lisbeth"
        class="intro-image"
      />
    </div>
    <div class="text-container header light">
      <h1>Psykoterapi & familiebehandling</h1>
      <h2>Nærvær, tryghed og forandring</h2>
    </div>
  </section>
  <section class="why-section">
    <div class="text-container lighter">
      <h2>Hvorfor psykoterapi?</h2>
      <p>{{ hvorforText }}</p>
    </div>
  </section>
  <section class="offerings-section">
    <div class="text-container light">
      <h2>Jeg tilbyder</h2>

      Til private:
      <ul>
        <li>Individuel terapi til voksne</li>
        <li>Parterapi</li>
        <li>Familieterapi</li>
        <li>Terapi til børn og unge</li>
      </ul>
      Til kommuner:
      <ul>
        <li>Terapi til børn og unge</li>
        <li>Familiebehandling (§30 og §32)</li>
        <li>
          Støtteperson til forældre, hvis barn er anbragt udenfor hjemmet (§ 75)
        </li>
        <li>Støtte til samvær</li>
      </ul>
    </div>
    <div class="image-container">
      <img
        src="@/assets/strand.jpg"
        alt="Udsigt af sti fra skovbryn mod strand. Der er en redningskrans synlig nede ved stranden"
      />
    </div>
  </section>
  <section class="contact-section">
    <div class="text-container lighter">
      <p>
        Vil du vil høre nærmere eller booke en tid, er du velkommen til at
        kontakte mig.
      </p>
      <button @click="goToContact">KONTAKT</button>
    </div>
  </section>
</template>

<script setup>
import hvorforText from "@/content/hvorfor_psykoterapi.txt?raw";
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

img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  display: block;
}

section {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: stretch;
  gap: var(--gap-size);
}

ul {
  display: flex;
  flex-direction: column;
  gap: 0.5rem;
}

.landing-section {
  max-height: calc(100vh - var(--navbar-height) - var(--gap-size));
}

.landing-section .image-container {
  flex: 2;
  min-width: 0;
}

.landing-section .text-container {
  flex: 3;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  letter-spacing: 0.06em;
  font-size: 1.3em;
}

.landing-section .text-container h1 {
  text-align: center;

}

.why-section .text-container {
  flex: 1;
}

.contact-section .text-container {
  flex: 1;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
  padding: 3rem 5rem;
}

.contact-section button {
  background-color: var(--farve-lighter);
}
button:hover {
  color: var(--farve-lighter);
  background-color: var(--farve-dark);
}

.offerings-section .image-container {
  flex: 2;
  min-width: 0;
}

.offerings-section .text-container {
  flex: 3;
}

.offerings-section .text-container h2 {
  margin-bottom: 0.4em;
}

.header-mobile {
  display: none;
}

.header h1 {
  font-weight: 500;
  margin-top: 0;
  margin-bottom: 0.2em;
  font-size: 1.8em;
}

.header h2 {
  font-weight: 100;
  font-size: 1.2em;
}

@media (max-width: 1200px) {
  section {
    display: flex;
    flex-direction: column;
  }

  .contact-section .text-container {
    flex-direction: column;
  }

  .text-container {
    padding: 2rem;
  }

  .landing-section .text-container {
    display: none;
  }

  .landing-section {
    flex-direction: column;
  }

  .header-mobile {
    display: flex;
    font-size: 0.8em;
  }

  .contact-section .text-container {
    padding: 2rem;
  }
}
</style>
