<template>
  <div class="app-container">
    <Header />
    <SideMenu />
    <MainBody />
    <BottomNav />
  </div>
</template>

<script>
import Header from './components/Header.vue';
/*import SideMenu from './components/SideMenu.vue';*/
import MainBody from './components/MainBody.vue';
/*import BottomNav from './components/BottomNav.vue';*/

export default {
  components: {
    Header,
    /*SideMenu,*/
    MainBody,
    /*BottomNav*/
  }
};
</script>

<style>
/* Apply a global reset to remove all margins and padding */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

html, body {
  margin: 0;
  padding: 0;
  height: 100%;
  width: 100%;
}

#app {
  height: 100%;
  width: 100%;
}

/* Main container styles */
.app-container {
  width: 490px;
  margin: 0 auto;  /* Center horizontally */
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  background-color: #f8f9fa; /* Optional background */
}

</style>
