<template>
  <section class="price-section">
    <div class="text-container light">
      <h2 class="price-header">Priser</h2>
      <div class="price-elements">
        <div class="price-element">
          <p>1-1 terapi voksne / 60 minutter</p>
          <p>700 kr.</p>
        </div>
        <div class="price-element">
          <p>Parterapi / 90 minutter</p>
          <p>1.050 kr.</p>
        </div>
        <div class="price-element">
          <p>Terapi til børn og unge / 60 minutter</p>
          <p>700 kr.</p>
        </div>
        <div class="price-element">
          <p>Familieterapi / 90 minutter</p>
          <p>1.050 kr.</p>
        </div>
      </div>
      <p>
        Er du studerende mellem 18 og 25 år, tilbyder jeg 1-1 terapi af 60
        minutters varighed for 550 kr. pr. session.
      </p>
      <p>Betaling sker efter hver terapisession via MobilePay.</p>
      <p>
        Afbud skal ske senest kl. 19.00 dagen før vores aftale.<br />Ved senere
        afbud eller udeblivelse opkræves det fulde honorar.
      </p>
      <div>
        <h2>Til kommuner</h2>
        <p>Kontakt mig for priser</p>
      </div>
    </div>
  </section>
</template>

<script setup></script>

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

.price-header {
  margin-bottom: -20px;
}

.price-section .text-container {
  flex: 1;
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  align-items: stretch;
  gap: 30px;
}

.price-element {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
  gap: 50px;
}

.price-elements {
  margin: 0 40px;
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  align-items: stretch;
  max-width: 600px;
  gap: 20px;
}

p {
  margin: 0;
}

hr {
  flex: 1;
  border: none;
  height: 1px;
  background-color: var(--farve-dark);
}

@media (max-width: 1200px) {
  .text-container {
    padding: 2rem;
  }

  .price-element {
    gap: 5px;
    font-size: 0.6em;
  }

  .price-elements {
    margin: 0;
    max-width: 300px;
  }
}
</style>
