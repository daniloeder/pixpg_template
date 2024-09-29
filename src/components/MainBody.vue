<template>
  <div class="container">
    <div class="main-body">
      <!-- Top Banner -->
      <div class="banner">
        <img src="./../assets/images/WEB BANNER - PIX PG3.webp" alt="Top Banner" class="banner-img" />
      </div>

      <!-- Notice Section with Sound Icon -->
      <div class="notice-section">
        <img src="./../assets/images/furlaBlue_voice_icon.webp" alt="Sound Icon" class="sound-icon" />
        <div class="notice-box">
          <!-- Notice content can be added here -->
        </div>
        <div class="notice-text">
          <span>
            Bem-vindo ao pixpg.app
            ~ 1.Três bônus grátis no seu primeiro depósito até 20 por cento
            ~ 2.Convide amigos e ganhe até 10 cada convidado!
          </span>
        </div>
      </div>

      <!-- Jackpot Section -->
      <div class="jackpot-section">
        <img src="./../assets/images/JACKPOT-PIXPG-ezgif.com-video-to-webp-converter.webp" alt="Jackpot" class="jackpot-img" />
      </div>

      <!-- Menu Section -->
      <div class="menu-section">
        <div class="menu-item">
          <div class="menu-item-text">Popular</div>
        </div>
        <div class="menu-item">
          <div class="menu-item-text">PG Slots</div>
        </div>
        <div class="menu-item">
          <div class="menu-item-text">PP Slots</div>
        </div>
        <div class="menu-item">
          <div class="menu-item-text">Evolution</div>
        </div>
        <div class="menu-item">
          <div class="menu-item-text">Convidar</div>
        </div>
      </div>

      <!-- Game Section -->
      <GameSection />
    </div>

    <footer class="footer">
      <!-- Footer content here -->
      Footer Content
    </footer>
  </div>
</template>

<script>
import GameSection from './GameSection.vue';

export default {
  name: 'MainBody',
  components: {
    GameSection,
  },
};
</script>

<style scoped>
/* Global styles */
html, body {
  height: 100%;
  margin: 0;
}

/* Container to hold header, main body, and footer */
.container {
  display: flex;
  flex-direction: column;
  height: 100vh; /* Full height of the viewport */
}

/* Main body styles */
.main-body {
  background-color: #8eaae1;
  background-image: url('./../assets/images/bg_pattern_tile.png');
  background-size: 10%;
  background-repeat: repeat;
  background-position: center bottom;
  background-attachment: fixed;
  flex: 1; /* Take up remaining space */
  padding: 0;
  overflow-y: auto; /* Enable vertical scrolling only */
}

/* Hide scrollbar for Webkit browsers (Chrome, Safari) */
.main-body::-webkit-scrollbar {
  display: none; /* Hide scrollbar */
}

/* Hide scrollbar for Firefox */
.main-body {
  scrollbar-width: none; /* Hide scrollbar */
}

/* Footer styles */
.footer {
  background-color: #014789; /* Adjust as needed */
  color: white;
  padding: 1rem; /* Adjust as needed */
}

/* Banner Styles */
.banner {
  width: 98%;
  text-align: center;
  border-radius: 1rem;
  margin: 0.5rem 1%;
}

.banner-img {
  width: 100%;
  height: 9.4rem;
  max-width: 100vw;
  border-radius: 0.5rem;
}

/* Notice Section */
.notice-section {
  display: flex;
  align-items: center;
  justify-content: space-between;
  background-color: #014789;
  border-top: 1px solid rgba(255, 255, 255, 0.1);
  border-bottom: 1px solid rgba(255, 255, 255, 0.1);
  padding: 0 5%;
  height: calc(min(100vw, 490px) * 0.08);
  margin-top: 0.7rem;
  box-sizing: border-box;
}

.sound-icon {
  width: calc(min(100vw, 490px) * 0.035);
  margin-left: -0.5rem;
}

.notice-box {
  flex: 1;
  text-align: center;
  color: rgba(255, 255, 255, 0.88);
  font-size: calc(min(100vw, 490px) / 750 * 22);
  font-weight: 700;
  margin-right: calc(min(100vw, 490px) * 0.016);
  font-family: Arial, Helvetica, sans-serif;
}

/* Notice text that scrolls */
.notice-text {
  color: white;
  white-space: nowrap; 
  text-align: center;
  font-weight: bold;
  font-size: calc(min(100vw, 490px) * 0.032);
  overflow: hidden; 
  width: 100%; 
  position: relative;
}

.notice-text span {
  display: inline-block;
  padding-left: 100%; 
  animation: scroll-left 40s linear infinite; 
}

@keyframes scroll-left {
  0% {
    transform: translateX(100%); 
  }
  100% {
    transform: translateX(-100%); 
  }
}

/* Jackpot Section */
.jackpot-section {
  text-align: center;
  margin: 0; 
  padding: 0; 
}

.jackpot-img {
  width: 100%;
  max-width: 100vw;
  display: block;
  margin: 0; 
}

/* Menu Section */
.menu-section {
  height: calc(min(100vw, 490px) * 0.16);
  width: 100%;
  background-color: #014789;
  display: flex;
  justify-content: space-evenly;
  padding: 1rem;
}

.menu-item {
  width: calc(min(100vw, 490px) * 0.16);
  align-items: center;
  justify-content: center;
  background-color: #0d273f;
  border-radius: 0.5rem;
  padding: 0.5rem;
}

.menu-item-text {
  color: rgba(255, 255, 255, 0.6);
  font-weight: 700;
  font-size: calc(min(100vw, 490px) / 750 * 22);
  font-family: Arial, Helvetica, sans-serif;
}

/* Game Section */
.game-section {
  width: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
  margin-top: 1rem;
}

.game-box {
  width: 100%;
  margin-left: calc(min(100vw, 490px) * 0.032);
}

.game-box-title {
  color: white;
  font-size: calc(min(100vw, 490px) * 0.032);
  font-weight: bold;
  font-family: Arial, Helvetica, sans-serif;
}

.games {
  width: 100%;
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  justify-content: flex-start;
  margin-top: 1rem;
}

.game {
  width: calc(min(100vw, 490px) / 750 * 218);
  height: calc(min(100vw, 490px) / 750 * 290);
  margin-right: calc(min(100vw, 490px) * 0.032);
  margin-bottom: calc(min(100vw, 490px) * 0.032);
  background-color: #0d273f;
  border-radius: 0.5rem;
  position: relative;
}

.game-img {
  width: 100%;
  height: 100%;
  border-radius: 0.5rem;
}

.game-title-box {
  width: 100%;
  height: 25%;
  font-size: calc(min(100vw, 490px) / 750 * 22);
  font-weight: bold;
  font-family: Arial, Helvetica, sans-serif;
  text-align: center;
  position: absolute;
  bottom: 0;
}

.game-title-text {
  color: white;
  font-size: calc(min(100vw, 490px) / 750 * 28);
  font-family: Arial, Helvetica, sans-serif;
  font-weight: 400;
}

.game-platform-text {
  color: white;
  font-size: calc(min(100vw, 490px) / 750 * 20);
  font-family: Arial, Helvetica, sans-serif;
  margin-top: 0.6rem;
  font-weight: 600;
}
</style>
