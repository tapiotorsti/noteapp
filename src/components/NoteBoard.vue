<template>
  <div class="noteboard">
    <NoteCard v-for="(note, index) in notes" :key="index" :note="note" />
    <div v-if="showModal" class="modal">
      <div class="modal-content">
        <span class="close-button" @click="$emit('closeModal')">×</span>
        <input v-model="newNote" placeholder="Enter note text" />
        <button @click="addNote">Save</button>
      </div>
    </div>
  </div>
</template>

<script>
import NoteCard from './NoteCard.vue';

export default {
  name: 'NoteBoard',
  components: {
    NoteCard,
  },
  props: ['showModal'],
  data() {
    return {
      newNote: '',
      notes: []
    }
  },
  methods: {
    addNote() {
      this.notes.push(this.newNote);
      this.newNote = '';
      this.$emit('closeModal');
    }
  }
}
</script>

<style lang="scss">
@import '../assets/noteboard.scss';
</style>
