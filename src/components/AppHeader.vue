<script>
import SearchBar from './SearchBar.vue'
import Button from './Button.vue'
import { store } from '../store.js'

export default {
  components: {
    SearchBar,
    Button
  },
  data() {
    return {

    }
  },
  methods: {
    searchContent() {
      console.log(`Sto facendo la ricerca di ${store.currentSearch}`)
    }
  }
}

</script>

<template>

  <div class="bg-secondary">
    <SearchBar />
    <Button @search="searchContent()" />
  </div>

</template>

<style></style>