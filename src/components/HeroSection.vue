<template>
  <section class="hero">
    <div class="hero__content">
      <h1>
        Transgourmet, le grossiste <br />
        alimentaire à<span class="marseille-text"
          >Marseille.
          <img
            class="vector-underline"
            src="../assets/vector-underline.svg
          "
            alt=""
          />
        </span>
      </h1>
      <p>
        Grâce à notre présence dans la cité phocéenne, les professionnels de la région
        bénéficient<br />
        depuis 2004 d'une solution d'approvisionnement complète.
      </p>
      <div class="hero__buttons">
        <button class="btn btn--primary">Envoyer mes informations</button>
        <button class="btn btn--outline"><span>Prendre contact</span></button>
      </div>
    </div>
    <div class="hero__image">
      <img src="../assets/camion-port.png" alt="Camion Transgourmet à Marseille" />
    </div>
  </section>
</template>

<style scoped>
.hero {
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: var(--section-padding);
  padding-top: 56px;
  padding-bottom: 0;
  gap: 3rem;
  text-align: center;
  overflow-x: hidden;
}

.hero h1 {
  margin-bottom: 1.5rem;
}

.marseille-text {
  position: relative;
  display: inline-block;
  margin-left: 20px;
}

.vector-underline {
  position: absolute;
  bottom: -15px;
  left: 0;
  width: 100%;
  height: auto;
  z-index: 1;
  animation: drawUnderline 1s ease-out 0.8s forwards;
  stroke-dasharray: 1000;
  stroke-dashoffset: 1000;
}
@keyframes drawUnderline {
  to {
    stroke-dashoffset: 0;
  }
}

.hero__buttons {
  margin-top: 2rem;
  display: flex;
  justify-content: center;
  gap: 1rem;
}

.hero__image {
  display: flex;
  justify-content: center;
  position: relative;
}

.hero__image img {
  width: 100vw;
  max-width: 100vw;
  height: auto;
  object-fit: cover;
  border-radius: 0;
  box-shadow: 0 8px 24px rgba(0, 0, 0, 0.1);
}

.btn {
  padding: 0.75rem 1.5rem;
  font-weight: 600;
  border: none;
  border-radius: 6px;
  cursor: pointer;
  transition: all 0.3s ease;
  margin-bottom: 92px;
}

.btn:hover {
  transform: translateY(-3px);
  box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
}

.btn:active {
  transform: translateY(-1px);
}

.btn--primary {
  background: var(--accent-color);

  color: white;
}

.btn--outline {
  border: 2px solid transparent;
  background-image:
    linear-gradient(white, white), linear-gradient(to right, var(--accent-color), #b10020, #800015);
  background-origin: border-box;
  background-clip: padding-box, border-box;
  position: relative;
}

.btn--outline span {
  background-image: linear-gradient(to right, var(--accent-color), #b10020, #800015);
  -webkit-background-clip: text;
  background-clip: text;
  color: transparent;
  display: block;
}
</style>
