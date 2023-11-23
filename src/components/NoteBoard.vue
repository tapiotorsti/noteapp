<template>
  <div class="noteboard">
    <NoteCard v-for="(note, index) in notes" :key="index" :note="note" />
    <add-note-modal :showModal="showModal" @add-note="addNote" @close="showModal = false" />

  </div>
</template>

<script>
import NoteCard from './NoteCard.vue';
import AddNoteModal from './AddNoteModal.vue';
import 'firebase/compat/firestore';
import { collection, addDoc } from 'firebase/firestore';
import { db } from '../main.js';

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
    async addNote(newNote) {
  // Add the new note to Firestore
  const notesCollection = collection(db, 'notes');

  try {
    const docRef = await addDoc(notesCollection, {
      title: newNote.title,
      content: newNote.content,
    });

    newNote.id = docRef.id;
    this.notes.push(newNote);
    this.closeModal();
  } catch (error) {
    console.error('Error adding note to Firestore: ', error);
  }
},
    closeModal() {
      console.log('Closing modal...');
      this.$emit('update:showModal', false);
    },
    openModal() {
      this.$emit('update:showModal', true); 
    },
  },
};
</script>

<style lang="scss">
@import '../assets/noteboard.scss';
</style>
