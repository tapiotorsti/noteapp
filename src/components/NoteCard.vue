<template>
  <div class="notecard">
    <h1>{{ note }}</h1>
  </div>
</template>

<script>
export default {
  name: 'NoteCard',
  props: ['note']
}
</script>

<style lang="scss">
@import '../assets/notecard.scss';
</style>
