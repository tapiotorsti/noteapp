<template>
    <div v-if="showModal" class="modal">
      <div class="modal-content">
        <span class="close-button" @click="closeModal">x</span>
        <input v-model="newNote" placeholder="Enter note text" />
        <button @click="addNote">Save</button>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    name: 'AddNoteModal',
    props: {
      showModal: Boolean,
    },
    data() {
      return {
        newNote: '',
      };
    },
    methods: {
      addNote() {
        if (this.newNote.trim()) {
          this.$emit('addNote', this.newNote);
          this.closeModal();
        }
      },
      closeModal() {
        this.newNote = '';
        this.$emit('closeModal');
      },
    },
  };
  </script>

<style lang="scss">
@import '../assets/addnotemodal.scss';
</style>
