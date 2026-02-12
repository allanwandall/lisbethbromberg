<template>
  <section class="libber-mobil">
    <div class="image-container">
      <img src="@/assets/libber4.jpg" alt="Billede af Lisbeth" />
    </div>
  </section>
  <section class="about-section">
    <div class="text-container light">
      <p>{{ omMigText }}</p>
    </div>
    <div class="image-container">
      <img src="@/assets/libber4.jpg" alt="Billede af Lisbeth" />
    </div>
  </section>
  <section class="education-section">
    <div class="text-container lighter">
      <div class="horizontal-flex">
        <p>
          Jeg er uddannet socialpædagog og psykoterapeut MPF (4-årig
          psykoterapeutuddannelse på <a href="https://seop.dk/">SEOP</a> -
          Skolen for Eksistentiel og Oplevelsesorienteret Psykoterapi).<br /><br />Jeg
          modtager løbende supervision og er medlem af
          <a href="https://psykoterapeutforeningen.dk/"
            >Dansk Psykoterapeutforening</a
          >
        </p>
        <div class="image-container">
          <img
            src="@/assets/mpf_logo.png"
            alt="Logo for Dansk Psykoterapeut Forening"
          />
        </div>
      </div>
      <div class="horizontal-flex">
        <div class="vertical-flex">
          <div>
            <h3>Uddannelse</h3>
            <ul>
              <li>
                Psykoterapeut ved SEOP (Skolen for Eksistentiel og
                Oplevelsesorienteret Psykoterapi)
              </li>
              <li>Socialpædagog ved Hindholm Socialpædagogiske Seminarium</li>
            </ul>
          </div>
          <div>
            <h3>Psykoterapeutiske træningsgrupper</h3>
            <ul>
              <li>
                Træningsgruppe i eksistentiel og oplevelsesorienteret
                psykoterapi
              </li>
              <li>
                Træningsgruppe i neuroaffektiv og kropsorienteret psykoterapi
              </li>
              <li>Træningsgruppe i eksistentiel psykoterapi</li>
            </ul>
          </div>
        </div>

        <div>
          <h3>Længerevarende kurser</h3>
          <ul>
            <li>Choktraume Release uddannelse</li>
            <li>Traumebehandling</li>
            <li>Seksualitet</li>
            <li>Senfølger efter seksuelle overgreb i barndommen</li>
            <li>
              Gennemgribende personligheds<wbr />forstyrrelser/<wbr />ADHD/<wbr />Autisme
            </li>
            <li>Samskabelse</li>
          </ul>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import omMigText from "@/content/om_mig.txt?raw";
</script>

<style scoped>
.text-container {
  padding: 5rem;
  overflow: hidden;
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
  margin: 0;
}

.about-section .text-container {
  flex: 3;
}

.about-section .image-container {
  flex: 2;
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  align-items: stretch;
  gap: var(--gap-size);
}

.about-section .image-container img {
  flex: 2;
  object-fit: cover;
  object-position: 33% 50%;
}

.education-section .text-container {
  flex: 1;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  align-items: stretch;
  gap: var(--gap-size);
}

.horizontal-flex {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: flex-start;
  gap: var(--gap-size);
}

.vertical-flex {
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  align-items: stretch;
  gap: var(--gap-size);
}

.education-section .image-container {
  width: 120px;
}

.libber-mobil {
  display: none;
}

p {
  margin: 0;
}

h3 {
  margin-bottom: 0.5em;
}

.libber-container {
  float: right;
  margin-left: var(--gap-size);
  margin-bottom: var(--gap-size);
  background-color: white;
  padding-bottom: var(--gap-size);
  padding-left: var(--gap-size);
  margin-top: -5rem;
  margin-right: -5rem;
  border-bottom-left-radius: 10px;
}

.libber-billede {
  max-width: 350px;
  max-height: 700px;
  width: auto;
  height: auto;
}

@media (max-width: 1200px) {
  .libber-billede {
    display: none;
  }

  .about-section .image-container {
    display: none;
  }

  .libber-mobil {
    display: flex;
  }

  .text-container {
    padding: 2rem;
  }

  .education-section {
    flex-direction: column;
  }

  .education-section .text-container {
    flex-direction: column;
    gap: 2rem;
  }

  .horizontal-flex {
    flex-direction: column;
  }

  .education-section .image-container {
    align-self: center;
  }
}
</style>
