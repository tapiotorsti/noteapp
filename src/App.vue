<template>
  <div id="app">
    <Header />
    <NoteBoard />
    <Footer />
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Footer from './components/Footer.vue'
import NoteBoard from './components/NoteBoard.vue';

export default {
  name: 'App',
  components: {
    Header,
    Footer,
    NoteBoard
  }
}
</script>

<style scoped>
/* Your CSS for App.vue goes here */
</style>