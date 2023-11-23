<template>
  <header>
    <h1>NoteApp</h1>
    <font-awesome-icon class="add-button" icon="plus" @click="$emit('openModal')" />

  </header>
</template>

<script>
import { library } from '@fortawesome/fontawesome-svg-core'
import { faPlus } from '@fortawesome/free-solid-svg-icons'
import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome'

library.add(faPlus)

export default {
name: 'NoteHeader',
components: {
  FontAwesomeIcon
}
}
</script>

<style lang="scss">
@import '../assets/noteheader.scss';
</style>