<template>
  <div class="w-64 bg-blue-800 text-white h-full fixed top-0 left-0 z-50 transform transition-transform"
       :class="{'-translate-x-full': !isOpen}">
    <button @click="toggleMenu" class="text-xl p-4">←</button>
    <nav class="p-4">
      <ul>
        <li class="mb-4"><a href="#" class="flex items-center space-x-2"><span>🔥</span><span>Popular</span></a></li>
        <li class="mb-4"><a href="#" class="flex items-center space-x-2"><span>🎰</span><span>PG Slots</span></a></li>
        <li class="mb-4"><a href="#" class="flex items-center space-x-2"><span>🎮</span><span>PP Slots</span></a></li>
        <li class="mb-4"><a href="#" class="flex items-center space-x-2"><span>📅</span><span>Eventos</span></a></li>
        <li class="mb-4"><a href="#" class="flex items-center space-x-2"><span>👑</span><span>VIP</span></a></li>
      </ul>
    </nav>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isOpen: false
    };
  },
  methods: {
    toggleMenu() {
      this.isOpen = !this.isOpen;
    }
  }
}
</script>

<style scoped>
/* Add styles for transitions if needed */
</style>
