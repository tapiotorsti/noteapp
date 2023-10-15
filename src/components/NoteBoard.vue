<template>
    <div class="noteboard">
      <h1>NoteApp</h1>
      <NoteCard />
    </div>
  </template>

<script>
import NoteCard from './NoteCard.vue';

export default {
  name: 'NoteBoard',
  components: {
    NoteCard, // Register the Note component for use in this template
  },
}
</script>

<style lang="scss">
@import '../assets/noteboard.scss';
</style>