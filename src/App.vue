<template>
  <div id="app">
    <NavBar/>
    <MainContent/>
    <FooterCom/>
  </div>

</template>

<script>
import NavBar from './components/NavBar.vue';
import FooterCom from './components/FooterCom.vue';
import MainContent from './components/MainContent.vue';

export default {
  name: 'App',
  components: {
    NavBar,
    MainContent,
    FooterCom
  }
}
</script>

<style>
body {
  background-color: #F8F8F8; /* Set the background color for the entire page */
}
</style>
