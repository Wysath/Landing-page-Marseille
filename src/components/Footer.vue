<template>
  <footer class="footer">
    <img src="../assets/logo-transgourmet.png" alt="Logo Transgourmet" class="footer__logo" />
    <nav>
      <ul class="footer__links">
        <li>Restauration commerciale</li>
        <li>Restauration collective</li>
        <li>Nos produits</li>
        <li>Nos filières</li>
        <li>Contact</li>
      </ul>
    </nav>
    <div class="footer__legal"><a href="#">Mentions légales</a> | <a href="#">CGU</a></div>
  </footer>
</template>

<style scoped>
.footer {
  padding: 3rem 2rem;
  background-color: var(--background-color-dark);
  text-align: center;
}

.footer__logo {
  height: 40px;
  margin-bottom: 1rem;
}

.footer__links {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 1rem;
  list-style: none;
  padding: 0;
  margin: 1rem 0;
  color: var(--text-color-light);
  padding-bottom: 64px;
}

.footer__legal {
  border-top: 1px solid var(--text-color-light);
  padding-top: 32px;
}

.footer__legal a {
  font-size: 0.875rem;
  color: var(--text-color-light);
  text-decoration: none;
}
</style>
