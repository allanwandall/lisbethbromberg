<template>
    <section class="about-section">
        <div class="text-container light">
            <p>{{ omMigText }}</p>
        </div>
        <div class="image-container">
            <img src="@/assets/Lisbeth.jpg" alt="Billede af Lisbeth"/>
        </div>
    </section>
    <section class="education-section">
        <div class="text-container lighter">
            <p>Jeg er uddannet socialpædagog og psykoterapeut MPF (4-årig psykoterapeutuddannelse på <a href="https://seop.dk/">SEOP</a> - Skolen for Eksistentiel og Oplevelsesorienteret Psykoterapi).<br /><br />Jeg modtager løbende supervision og er medlem af <a href="https://psykoterapeutforeningen.dk/">Dansk Psykoterapeutiskforening</a></p>
            <div class="image-container">
                <img src="@/assets/mpf_logo.png" alt="Logo for Dansk Psykoterapeut Forening"/>
            </div>
        </div>
    </section>
    
</template>

<script setup>
import omMigText from '@/content/om_mig.txt?raw'
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

.about-section .text-container {
    flex: 2;
}

.about-section .image-container {
    flex: 1;
}

.education-section .text-container {
    flex: 1;
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
    gap: 90px;
}

.education-section .image-container {
    width: 90px;
}
</style>