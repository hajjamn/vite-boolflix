<script>
import { store } from '../store.js'

export default {
  data() {
    return {
      store,
    }
  }
}

</script>

<template>

  <div class="me-3 flex-grow-1">
    <input type="text" class="form-control" id="header-searchbar"
      placeholder="Cerca il titolo del tuo film o della tua serie..." v-model="store.currentSearch"
      @keyup.enter="$emit('search')"></input>
  </div>

</template>

<style></style>