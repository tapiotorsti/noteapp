<template>
  <div class="noteboard">
    <NoteCard v-for="(note, index) in notes" :key="index" :note="note" />
    <add-note-modal :showModal="showModal" @addNote="addNote" @closeModal="closeModal" />
  </div>
</template>

<script>
import NoteCard from './NoteCard.vue';
import AddNoteModal from './AddNoteModal.vue';

export default {
  name: 'NoteBoard',
  components: {
    NoteCard,
    AddNoteModal,
  },
  props: ['showModal'],
  data() {
    return {
      notes: [],
    };
  },
  methods: {
    addNote(newNote) {
      this.notes.push(newNote);
      this.closeModal();
    },
    closeModal() {
      this.$emit('closeModal');
    },
  },
};
</script>

<style lang="scss">
@import '../assets/noteboard.scss';
</style>
