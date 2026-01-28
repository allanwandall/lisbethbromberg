<template>
    <section class="adults-section">
        <div class="text-container light">
            <h2>Terapi til voksne</h2>
            <p>{{ terapiVoksneText }}</p>
        </div>
        <div class="image-container">
            <img src="@/assets/strand.jpg" alt="Strand placeholder"/>
        </div>
    </section>
    <section class="example-section">
        <div class="text-container lighter">
            <div>
                <p>Eksempler på temaer:</p>
                <ul>
                    <li>et ønske om at lære dig selv bedre at kende og blive fortrolig med dine egne følelser og sansninger</li>
                    <li>problemer med selvværd</li>
                    <li>et stort fokus på, hvad andre tænker om dig</li>
                    <li>mangel på kærlighed og tillid i nære relationer</li>
                    <li>været udsat for vold eller overgreb, og kæmper med senfølger</li>
                </ul>
            </div>
            <div>
                <p>Måske er du:</p>
                <ul>
                    <li>pårørende til mennesker i sorg og krise</li>
                    <li>pårørende til mennesker med særlige behov</li>
                    <li>ensom, sorgfuld, stresset eller angst</li>
                </ul>
                <p>Uanset hvad du føler udfordrende eller begrænsende i dit liv, er du velkommen til at tage kontakt.</p>
            </div>
        </div>
    </section>
    <section>
        <div class="text-container light">
            <h2>Parterapi</h2>
            <p>{{ parterapiText }}</p>
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
import terapiVoksneText from '@/content/terapi_voksne.txt?raw'
import parterapiText from '@/content/parterapi.txt?raw'
import boernText from '@/content/boern_kommune.txt?raw'
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

.adults-section .text-container {
    flex: 2;
}

.adults-section .image-container {
    flex: 1;
}

.example-section .text-container div {
    flex: 1;
    display: flex;
    flex-direction: column;
    justify-content: flex-start;
    align-items: flex-start;
}

.example-section .text-container {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: flex-start;
    gap: 200px;
}

</style>