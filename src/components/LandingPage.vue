<template>
<section class="intro-section">
    <div class="image-container">
        <img src="@/assets/lisbeth_billede.webp" alt="Billede af Lisbeth" class="intro-image" />
    </div>
    <div class="text-container">
        <h2>Hvorfor psykoterapi?</h2>
        <p>{{ aboutText }}</p>
    </div>
</section>
<section class="theme-section">
    <div class="text-container">
        <h2>Eksempler på temaer</h2>
        <ul>
            <li>Et ønske om at lære dig selv bedre at kende og blive fortrolig med dine egne følelser og sansninger</li>
            <li>Problemer med selvværd</li>
            <li>Fokus på hvad andre tænker om dig</li>
            <li>At være pårørende til mennesker i sorg og krise</li>
            <li>At være pårørende til mennesker med særlige behov</li>
            <li>Mangel på kærlighed og tillid i nære relationer</li>
            <li>Ensomhed</li>
            <li>Sorg</li>
            <li>Stress</li>
            <li>Angst</li>
        </ul>
    </div>
    <div class="image-container">
        <img src="@/assets/lisbergbrombethlogo.png" alt="Logo" class="theme-image" />
    </div>
    <!-- <div class="image-placeholder">
        BILLEDE PLACEHOLDER
    </div> -->
</section>
</template>

<script setup>
import aboutText from '@/content/about.txt?raw'

</script>

<style scoped>
section {
    margin: 0 4rem;
}

.text-container {
    padding: 5rem;
}

.intro-section {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: stretch;
    gap: 3rem;
}

.intro-section .image-container {
    flex: 1;
    min-width: 0;    
}

img {
    width: 100%;
    height: 100%;
    object-fit: cover;
    display: block;
    border-radius: 0.5rem;
}

.intro-section .text-container {
    flex: 2;
}

.theme-section .text-container {
    flex: 3;
}

.theme-section {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: stretch;
    gap: 3rem;
}

.theme-section .image-placeholder {
    flex: 2;
    display: flex;
    justify-content: center;
    align-items: center;
}

.theme-section .image-container {
    flex: 2;
    min-width: 0;    
}

</style>