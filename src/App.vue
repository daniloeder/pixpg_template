<template>
  <div id="app" class="app-container">
    <Header />
    <MainBody />
    <BottomNav />
  </div>
</template>

<script>
import Header from './components/Header.vue';
import MainBody from './components/MainBody.vue';
import BottomNav from './components/BottomNav.vue';

export default {
  components: {
    Header,
    MainBody,
    BottomNav,
  },
};
</script>

<style>
/* Reset margins and paddings */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

html, body {
  height: 100%;
  width: 100%;
  overflow: hidden; /* Prevent body from scrolling */
}

#app {
  height: 100%;
  width: 100%;
}

/* Layout configuration */
.app-container {
  display: flex;
  flex-direction: column;
  height: 100%;
  max-width: 490px;
  margin: 0 auto;
}

/* Header should be fixed at the top */
header {
  position: fixed;
  top: 0;
  width: 100%;
  max-width: 490px;
  background-color: #f8f9fa; /* Background color for the header */
  z-index: 1000;
}

/* MainBody should take up the available space and scroll */
.main-body {
  flex: 1;
  overflow-y: auto;
  margin-top: 60px; /* Adjust according to header height */
  margin-bottom: 60px; /* Adjust according to footer height */
}

/* BottomNav should be fixed at the bottom */
footer {
  position: fixed;
  bottom: 0;
  width: 100%;
  max-width: 490px;
  background-color: #014789;
  z-index: 1000;
}
</style>
