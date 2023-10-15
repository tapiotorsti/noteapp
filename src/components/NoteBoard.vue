<template>
    <div class="noteboard">
      <NoteCard />
    </div>
  </template>

<script>
import NoteCard from './NoteCard.vue';

export default {
  name: 'NoteBoard',
  components: {
    NoteCard,
  },
}
</script>

<style lang="scss">
@import '../assets/noteboard.scss';
</style>