<template>
  <header class="bg-custom-blue p-4 text-white flex justify-between items-center w-full">
    <!-- Menu Icon (left-aligned) -->
    <img src="./../assets/images/header_menu_icon.webp" alt="Menu Icon" class="w-6 h-6 md:w-8 md:h-8">

    <!-- Centered Logo -->
    <div class="flex-1 text-center">
      <img src="./../assets/images/logopixpg.webp" alt="Fortune Ox Logo" class="mx-auto w-24">
    </div>

    <!-- Buttons (right-aligned) -->
    <nav class="flex space-x-2">
      <button class="bg-login-btn-bg text-login-btn-text border-login-btn-border border-2 p-2 rounded-md">
        Login
      </button>
      <button class="bg-register-btn-bg text-register-btn-text border-register-btn-border border-2 p-2 rounded-md">
        Register
      </button>
    </nav>
  </header>
</template>

<script>
export default {
  name: 'AppHeader',  // Multi-word component name
};
</script>

<style scoped>
/* Define custom colors */
.bg-custom-blue {
  background-color: #014789;
  height: 3.5rem;  /* Adjusted for better appearance */
}

/* Button styles */
.bg-login-btn-bg {
  background-color: #FFFCD2;
  border-radius: 0.5rem;
  padding: 0.5rem 1rem;
}

.text-login-btn-text {
  color: #014789;
}

.border-login-btn-border {
  border-color: #014789;
  border-width: 1px;
}

.bg-register-btn-bg {
  background-color: #014789;
  border-radius: 0.5rem;
  padding: 0.5rem 1rem;
}

.text-register-btn-text {
  color: #FFFCD2;
}

.border-register-btn-border {
  border-color: #FFFCD2;
  border-width: 1px;
}

/* Centering logo and adjusting button layout */
.w-full {
  width: 100%;
}

.mx-auto {
  margin-left: auto;
  margin-right: auto;
}

/* Flexbox adjustments */
.flex-1 {
  flex: 1;
}

.space-x-2 > * + * {
  margin-left: 0.5rem; /* Space between buttons */
}
</style>
