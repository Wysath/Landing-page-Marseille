<template>
  <section class="delivery">
    <div class="delivery__text">
      <div class="delivery__text-left">
        <span>La livraison</span>
        <h2>La proximité entre nous</h2>
      </div>
      <div class="delivery__text-right">
        <p>
          En favorisant les circuits courts et les filières responsables, Transgourmet s’engage aux
          côtés des restaurateurs marseillais pour leur permettre de proposer à leurs clients des
          produits frais et savoureux, reflétant l’excellence du terroir local. Une véritable
          alliance entre tradition, qualité et innovation au service de la gastronomie régionale.
        </p>
        <button class="btn btn--outline">Détails sur la livraison</button>
      </div>
    </div>
    <div class="delivery__image">
      <img src="../assets/camion-route.png" alt="Camion Transgourmet sur la route" />
    </div>
  </section>
</template>

<style scoped>
.delivery {
  margin-left: 124px;
  margin-right: 124px;
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  gap: 2rem;
  padding: var(--section-padding);
}

.delivery__text {
  display: flex;
  flex: 1 1 400px;
  gap: 2rem;
  animation: fadeIn 0.8s ease-out forwards;
}

.delivery__text-left {
  flex: 1;
  animation: slideInLeft 0.8s ease-out 0.2s backwards;
}

.delivery__text-right {
  flex: 1;
  animation: slideInRight 0.8s ease-out 0.4s backwards;
}

.delivery__image {
  display: flex;
  justify-content: center;
  width: 100%;
  animation: fadeInUp 1s ease-out 0.6s backwards;
}

.delivery__image img {
  justify-content: center;
  max-width: 100%;
  border-radius: 10px;
  box-shadow: 0 8px 24px rgba(0, 0, 0, 0.1);
  transition: transform 6s ease-in-out;
}

.delivery__image:hover img {
  transform: translateX(5px) translateY(-2px);
}

/* Animations pour le bouton */
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

.btn:hover {
  transform: translateY(-3px);
  box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
}

.btn:active {
  transform: translateY(-1px);
}

span {
  background-size: 200% auto;
  animation: shimmer 3s infinite;
  background-image: linear-gradient(
    to right,
    var(--accent-color),
    #b10020,
    #800015,
    #b10020,
    var(--accent-color)
  );
  -webkit-background-clip: text;
  background-clip: text;
  color: transparent;
  display: inline-block;
  font-weight: var(--font-weight-bold);
  margin-bottom: 8px;
}

@keyframes fadeIn {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
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

@keyframes slideInRight {
  from {
    opacity: 0;
    transform: translateX(50px);
  }
  to {
    opacity: 1;
    transform: translateX(0);
  }
}

@keyframes shimmer {
  0% {
    background-position: 0% center;
  }
  50% {
    background-position: 100% center;
  }
  100% {
    background-position: 0% center;
  }
}
</style>
