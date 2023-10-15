<template>
    <div class="noteboard">
      <h1>NoteApp</h1>
      <Note />
    </div>
  </template>

<script>
import Note from './Note.vue';

export default {
  name: 'NoteBoard',
  components: {
    Note, // Register the Note component for use in this template
  },
}
</script>

<style lang="scss">
@import '../assets/noteboard.scss';
</style>