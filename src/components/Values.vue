<template>
  <section class="values">
    <span>L'engagement</span>
    <h2 class="values__title">Notre promesse pour vous</h2>
    <div class="values__cards">
      <article class="card" v-for="(value, i) in values" :key="i">
        <div class="card__icon">
          <img :src="value.icon" :alt="`Icône ${value.title}`" />
        </div>
        <h3>{{ value.title }}</h3>
        <p>{{ value.text }}</p>
      </article>
    </div>
  </section>
</template>

<script setup>
import boutiqueIcon from '../assets/boutique.png'
import completIcon from '../assets/complet.png'
import clefIcon from '../assets/clef.png'

const values = [
  {
    title: 'Le grossiste de la restauration',
    text: 'Transgourmet, grossiste alimentaire de référence, fournit une large gamme de produits adaptés aux restaurateurs, qu ils soient indépendants ou organisés.',
    icon: boutiqueIcon,
  },
  {
    title: 'Un partenaire complet',
    text: 'Transgourmet, grossiste pour restaurants, propose une offre complète de produits frais, surgelés, épicerie, hygiène et emballage. Grâce à une logistique optimisée, il assure des livraisons rapides et fiables pour un approvisionnement de qualité.',
    icon: completIcon,
  },
  {
    title: 'Un service personnalisé',
    text: 'Choisir Transgourmet, c’est opter pour un service personnalisé, une expertise reconnue et un accompagnement sur mesure. Avec une présence nationale et une offre adaptée aux tendances, il est le partenaire de confiance des restaurateurs.',
    icon: clefIcon,
  },
]
</script>

<style scoped>
span {
  color: linear-gradient(to right, var(--accent-color), #b10020, #800015);
}

.values {
  padding: var(--section-padding);
  text-align: center;
  background-color: #f7f7f7;
}

.values__title {
  margin-bottom: 3rem;
}

span {
  background-image: linear-gradient(to right, var(--accent-color), #b10020, #800015);
  -webkit-background-clip: text;
  background-clip: text;
  color: transparent;
  display: inline-block;
  font-weight: var(--font-weight-bold);
  margin-bottom: 8px;
}

h3 {
  color: var(--accent-color);
}

.values__cards {
  display: flex;
  flex-wrap: wrap;
  gap: 2rem;
  justify-content: center;
}

.card {
  width: 378.67px;
  padding: 24px;
  background-color: var(--background-color);
  border-radius: 10px;
  text-align: left;
  transition: transform 0.3s ease;
}

.card:hover {
  transform: translateY(-6px);
  box-shadow: 0 10px 25px rgba(0, 0, 0, 0.07);
}

@keyframes fadeInUp {
  from {
    opacity: 0;
    transform: translateY(30px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

.values__cards .card:nth-child(1) {
  animation: fadeInUp 0.6s ease-out 0.2s backwards;
}

.values__cards .card:nth-child(2) {
  animation: fadeInUp 0.6s ease-out 0.4s backwards;
}

.values__cards .card:nth-child(3) {
  animation: fadeInUp 0.6s ease-out 0.6s backwards;
}

.card__icon {
  margin-bottom: 1rem;
  height: 48px;
  display: flex;
  align-items: center;
}

.card__icon img {
  max-height: 100%;
  width: auto;
}
</style>
