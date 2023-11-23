<template>
  <div id="app">
    <NoteHeader @openModal="showModal = true" />
    <NoteBoard :showModal="showModal" @addNote="addNote" @update:showModal="showModal = $event" />
    <NoteFooter />
  </div>
</template>

<script>
import NoteHeader from './components/NoteHeader.vue';
import NoteFooter from './components/NoteFooter.vue';
import NoteBoard from './components/NoteBoard.vue';

export default {
  name: 'App',
  components: {
    NoteHeader,
    NoteFooter,
    NoteBoard,
  },
  data() {
    return {
      showModal: false,
    };
  },
  watch: {
    showModal(newVal) {
      console.log('showModal changed:', newVal);
    },
  },
  methods: {
    addNote() {
      this.showModal = false;
    },
  },
};
</script>


<style scoped>
/* CSS goes here */
</style>
