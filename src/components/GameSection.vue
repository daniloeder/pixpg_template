<template>
    <div class="game-section">
      <!-- Loop through the game sections array and display each section -->
      <div v-for="(section, sectionIndex) in gameSections" :key="sectionIndex" class="game-box">
        <!-- Section title -->
        <div class="game-box-title">{{ section.title }}</div>
        <div class="games">
          <!-- Loop through the games array for each section and display each game -->
          <div v-for="(game, gameIndex) in section.games" :key="gameIndex" class="game">
            <img :src="game.image" :alt="game.title" class="game-img">
            <div class="game-title-box">
              <div class="game-title-text">{{ game.title }}</div>
              <div class="game-platform-text">{{ game.platform }}</div>
            </div>
          </div>
        </div>
        <div class="more-games-box">
          <div class="more-games-btn">+ Carregar mais</div>
        </div>
      </div>
    </div>
  </template>
  
  <script>
  import PGSlotImage from '@/assets/images/PG-SLOT-093.png.webp';
  import MGSlotImage from '@/assets/images/PG-SLOT-093.png.webp';
  
  export default {
    name: 'GameSection',
    data() {
      return {
        gameSections: [
          {
            title: 'PG Slots',
            games: [
              {
                title: 'PG Slots 1',
                platform: 'PG',
                image: PGSlotImage,
              },
              {
                title: 'PG Slots 2',
                platform: 'PG',
                image: PGSlotImage,
              },
              {
                title: 'PG Slots 3',
                platform: 'PG',
                image: PGSlotImage,
              },
              {
                title: 'PG Slots 4',
                platform: 'PG',
                image: PGSlotImage,
              },
            ],
          },
          {
            title: 'MG Slots', // Title of the second game section
            games: [
              {
                title: 'MG Slots 1',
                platform: 'MG',
                image: MGSlotImage,
              },
              {
                title: 'MG Slots 2',
                platform: 'MG',
                image: MGSlotImage,
              },
              {
                title: 'MG Slots 3',
                platform: 'MG',
                image: MGSlotImage,
              },
              {
                title: 'MG Slots 4',
                platform: 'MG',
                image: MGSlotImage,
              },
            ],
          },
        ],
      };
    },
  };
  </script>
  
  <style scoped>
  .game-section {
    width: 100%;
    grid-column: span 4;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    margin-top: 1rem;
  }
  
  .game-box {
    width: 100%;
    margin-left: calc(min(100vw, 490px) * 0.032);
    margin-bottom: 2rem; /* Adds space between sections */
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
  
  .more-games-box {
    width: 100%;
    display: flex;
    justify-content: center;
    margin-top: 1rem;
  }
  
  .more-games-btn {
    color: white;
    font-size: calc(min(100vw, 490px) / 750 * 22);
    font-family: Arial, Helvetica, sans-serif;
    cursor: pointer;
  }
  </style>
  