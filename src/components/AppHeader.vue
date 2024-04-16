<script>
import SearchBar from './SearchBar.vue'
import Button from './Button.vue'

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
      console.log('Sto facendo la ricerca')
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