<template>
  <div id="app">
    <NoteHeader @openModal="showModal = true" />
    <NoteBoard :showModal="showModal" @closeModal="showModal = false"/>
    <NoteFooter />
  </div>
</template>

<script>
import NoteHeader from './components/NoteHeader.vue'
import NoteFooter from './components/NoteFooter.vue'
import NoteBoard from './components/NoteBoard.vue';

export default {
  name: 'App',
  components: {
    NoteHeader,
    NoteFooter,
    NoteBoard
  },
  data() {
    return {
      showModal: false
    }
  }
}
</script>

<style scoped>
/* Your CSS for App.vue goes here */
</style>
