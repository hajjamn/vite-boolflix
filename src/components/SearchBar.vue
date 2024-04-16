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

  <div>
    <div class="mb-3">
      <label for="header-searchbar" class="form-label">I am a SearchBar
        Label</label>
      <input type="text" class="form-control" id="header-searchbar" placeholder="I am a searchbar"
        v-model="store.currentSearch" @keyup.enter="$emit('search')"></input>
    </div>
  </div>

</template>

<style></style>