<template>
  <section class="producers">
    <div class="decoration">
      <img src="../assets/decoration.svg" alt="Producers" class="producers__image" />
    </div>
    <div class="producers__content">
      <div class="producers__left">
        <span class="gradient-text">L'engagement</span>
        <h2>
          Transgourmet et <br />
          ses producteurs
        </h2>
      </div>
      <div class="producers__right">
        <p>
          Transgourmet s’appuie sur un réseau de producteurs partenaires en région marseillaise pour
          offrir aux professionnels de la restauration des produits de qualité, locaux et
          responsables. En valorisant les savoir-faire régionaux, nous soutenons l’économie locale
          tout en garantissant un approvisionnement fiable et diversifié.
        </p>
        <button class="btn btn--outline">Nos filières locales</button>
      </div>
    </div>
  </section>
</template>

<style scoped>
.producers {
  position: relative;
  margin-left: 124px;
  margin-right: 124px;
  padding: var(--section-padding);
  text-align: center;
}

.decoration {
  position: absolute;
  top: 0px;
  left: -120px;
}

.producers__content {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  gap: 2rem;
  text-align: left;
}

.producers__left,
.producers__right {
  animation: slideInLeft 1s ease-out;
  flex: 1;
}

@keyframes slideInLeft {
  from {
    opacity: 0;
    transform: translateX(-50px);
  }
  to {
    opacity: 1;
    transform: translateX(0);
  }
}

.gradient-text {
  background-image: linear-gradient(to right, var(--accent-color), #b10020, #800015);
  -webkit-background-clip: text;
  background-clip: text;
  color: transparent !important;
  display: inline-block;
  font-weight: var(--font-weight-bold);
  margin-bottom: 8px;
}

.producers__right p {
  margin: 1rem 0 2rem;
  max-width: 700px;
  font-size: 32px;
  line-height: 130%;
}

.btn {
  padding: 0.75rem 1.5rem;
  font-weight: 600;
  border: none;
  border-radius: 6px;
  cursor: pointer;
  transition: all 0.3s ease;
}

.btn--outline {
  background-color: transparent;
  border: 2px solid var(--accent-color);
  color: var(--accent-color);
}
</style>
