<template>
  <div>
    <Header />
    <SideMenu />
    <MainBody />
    <BottomNav />
  </div>
</template>

<script>
import Header from './components/Header.vue';
import SideMenu from './components/SideMenu.vue';
import MainBody from './components/MainBody.vue';
import BottomNav from './components/BottomNav.vue';

export default {
  components: {
    Header,
    SideMenu,
    MainBody,
    BottomNav
  }
}
</script>

<style>
/* Global styles if needed */
</style>
