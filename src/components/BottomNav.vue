<template>
  <footer class="footer-nav">
    <a href="#" class="nav-item text-center">
      <span>🏠</span>
      <p>Inicio</p>
    </a>
    <a href="#" class="nav-item text-center">
      <span>📅</span>
      <p>Eventos</p>
    </a>
    <a href="#" class="nav-item text-center">
      <span>💰</span>
      <p>Depósito</p>
    </a>
    <a href="#" class="nav-item text-center">
      <span>🛠</span>
      <p>Suporte</p>
    </a>
    <a href="#" class="nav-item text-center">
      <span>👤</span>
      <p>Perfil</p>
    </a>
  </footer>
</template>

<style scoped>
.footer-nav {
  background-color: #014789;
  color: white;
  display: flex;
  justify-content: space-around;
  padding: 1rem;
  position: fixed;
  bottom: 0;
  width: 100%;
  max-width: 490px;
  z-index: 1000;
}

.nav-item {
  display: flex;
  flex-direction: column;
  align-items: center;
  font-size: 0.9rem;
}

.nav-item span {
  font-size: 1.5rem;
}
</style>
