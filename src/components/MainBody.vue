<template>
  <main class="bg-white p-4 flex flex-col items-center">
    <section class="bg-blue-500 text-white p-8 text-center rounded-lg w-full mb-4">
      <h1 class="text-3xl font-bold">Jogar Agora com Fortune Ox!</h1>
      <button class="bg-yellow-400 text-blue-900 px-6 py-2 rounded mt-4">Jogar Agora!</button>
    </section>

    <!-- Featured Games Grid -->
    <section class="grid grid-cols-2 gap-4 w-full">
      <div v-for="game in games" :key="game.id" class="bg-white rounded-lg shadow p-4 text-center">
        <img :src="game.image" alt="game.title" class="w-full h-40 object-cover rounded-lg mb-2">
        <p class="text-lg font-bold">{{ game.title }}</p>
      </div>
    </section>
  </main>
</template>

<script>
export default {
  data() {
    return {
      games: [
        { id: 1, title: 'Fortune Tiger', image: 'path-to-image-1.png' },
        { id: 2, title: 'Fortune Rabbit', image: 'path-to-image-2.png' },
        { id: 3, title: 'Dragon Hatch', image: 'path-to-image-3.png' },
        { id: 4, title: 'Fortune Ox', image: 'path-to-image-4.png' }
      ]
    };
  }
}
</script>

<style scoped>
/* Add custom styles here */
</style>
