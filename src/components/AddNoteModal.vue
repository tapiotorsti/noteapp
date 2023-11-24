<template>
  <div v-if="showModal">
    <div class="modal-content add-note-modal">
      <span class="close-button" @click="closeModal">x</span>
      <div class="input-container">
        <input v-model="content" placeholder=" " />
      </div>
      <div class="save-button-container">
        <button class="save-button" @click="addNote">Save</button>
      </div>
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
      emit('update:showModal', false);
    };


    const addNote = () => {
      const newNote = {
        title: title.value,
        content: content.value,
      };

      // Emit the 'addNote' event with the new note data
      emit('add-note', newNote);

      // Emit the 'closeModal' event
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
