<template>
  <div v-if="showModal" class="modal">
    <div class="modal-content">
      <span class="close-button" @click="closeModal">x</span>
      <input v-model="content" placeholder="Enter note text" />
      <button @click="addNote">Save</button>
    </div>
  </div>
</template>

<script>
import { ref } from 'vue';

export default {
  name: 'AddNoteModal',
  props: ['showModal'],
  setup(props, { emit }) {
    const title = ref('');
    const content = ref('');

    const closeModal = () => {
  emit('close');
};
    const addNote = () => {
      const newNote = {
        title: title.value,
        content: content.value,
      };

      // Emit the 'addNote' event with the new note data
      emit('add-note', newNote);

      // Emit the 'closeModal' event to request the parent to close the modal
      closeModal();
    };

    return {
      title,
      content,
      addNote,
      closeModal,
    };
  },
};
</script>

<style lang="scss">
@import '../assets/addnotemodal.scss';
</style>
