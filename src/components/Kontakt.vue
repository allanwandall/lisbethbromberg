<template>
  <div class="card-stage">
    <div class="card-inner" id="businessCard">
      <div class="card-front lighter">
        <div class="belt">
          <img src="@/assets/logo_lighter.png" alt="Logo" class="logo" />
        </div>
        <div class="text">
          <h1>Lisbeth Bromberg</h1>
          <div>
            <p>
              <a href="https://www.lisbethbromberg.dk"
                >www.lisbethbromberg.dk</a
              >
            </p>
            <p>lisbethbromberg@protonmail.com</p>
            <p>93 80 99 82</p>
          </div>
          <div>
            <p>Norvangen 3D</p>
            <p>Opgang A, 2. Sal</p>
            <p>4220 Korsør</p>
          </div>
        </div>
      </div>
      <div class="card-back lighter">
        <ul>
          <li>Terapi for voksne, unge og børn</li>
          <li>Parterapi</li>
          <li>Familiebehandling</li>
          <li>Rådgivnings- og gruppeforløb</li>
        </ul>
        <img
          src="@/assets/mpf_logo_hvid.png"
          alt="Logo for Dansk Psykoterapeutforening"
          class="ptf-logo"
        />
        <img
          src="@/assets/libberlogo_lysg.png"
          alt="Logo for Lisbeth Bromberg"
          class="libber-logo"
        />
      </div>
    </div>
  </div>
  <button @click="flipCard">Vend kortet</button>
</template>

<script setup>
function flipCard() {
  document.getElementById("businessCard").classList.toggle("is-flipped");
}
</script>

<style scoped>
.card-stage {
  align-self: center;
  height: 60vh;
  width: calc(60vh * 1.75);
  perspective: 3000px;
  margin: 20px var(--gap-size) 0;
  position: relative;
}

.card-inner {
  position: absolute;
  width: 100%;
  height: 100%;

  transition: transform 0.6s cubic-bezier(0.4, 0, 0.2, 1);
  transform-style: preserve-3d;
}

.is-flipped {
  transform: rotateY(180deg);
}

.card-back,
.card-front {
  position: absolute;
  width: 100%;
  height: 100%;
  backface-visibility: hidden;
  border-radius: 2cqh;
  box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
}

.card-back {
  transform: rotateY(180deg);
  position: relative;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  gap: 5%;
  background-color: var(--farve-logo);
  color: white;
  overflow: hidden;
}

.card-back li {
  font-size: 4vh;
  letter-spacing: 0.1cqh;
}

.ptf-logo {
  width: 5%;
}

.libber-logo {
  position: absolute;
  right: -10%;
  bottom: -35%;
  height: 150%;
  z-index: -2;
}

.card-front {
  display: flex;
  flex-direction: row;
  justify-content: flex-start;
  align-items: stretch;
  gap: 6%;
  color: var(--farve-logo);
}

.belt {
  background-color: var(--farve-logo);
  min-width: 25%;
  max-width: 25%;
  margin-left: 10%;
  display: flex;
  justify-content: center;
  align-items: center;
}

.belt img {
  width: 90%;
}

.text {
  font-weight: lighter;
  display: flex;
  flex-direction: column;
  justify-content: space-evenly;
  align-items: flex-start;
}

.text div {
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  align-items: flex-start;
  gap: 10px;
}

.card-front h1 {
  font-size: 6vh;
  font-weight: lighter;
  margin: 0;
}

.card-front h2 {
  font-size: 4vh;
  font-weight: lighter;
  margin: 0;
}

.card-front p {
  font-size: 3vh;
  margin: 0;
}

button {
  align-self: center;
}

@media (max-width: 768px) {
  .card-stage {
    width: calc(100vw - (2 * var(--gap-size)));
    height: calc((100vw - (2 * var(--gap-size))) * 0.57);
    perspective: 1000px;
    margin: 20px var(--gap-size) 0;
  }

  .card-front h1 {
    font-size: 6vw;
  }

  .card-front h2 {
    font-size: 7vw;
  }

  .card-front p {
    font-size: 3vw;
  }

  .text div {
    gap: 0;
  }

  .card-back li {
    font-size: 4vw;
  }

  ul {
    padding-left: 5px;
  }
}
</style>
