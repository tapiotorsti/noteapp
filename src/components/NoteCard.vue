<template>
  <div class="notecard">
    <p>{{ note.content }}</p>
  </div>
</template>

<script>
export default {
  name: 'NoteCard',
  props: {
    note: Object,
  },
};
</script>

<style lang="scss">
@import '../assets/notecard.scss';
</style>
