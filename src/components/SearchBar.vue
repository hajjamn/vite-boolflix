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
      <label for="exampleFormControlTextarea1" class="form-label">I am a SearchBar
        Label</label>
      <textarea class="form-control" id="exampleFormControlTextarea1" rows="1" placeholder="I am a searchbar"
        v-model="store.currentSearch"></textarea>
    </div>
  </div>

</template>

<style></style>