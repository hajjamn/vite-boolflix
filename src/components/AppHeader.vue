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
  }
}

</script>

<template>

  <header class="bg-dark">
    <div class="container">
      <div class="row align-items-center">
        <div class="col-6">
          <h1 class="text-danger">Boolflix</h1>
        </div>
        <div class="col-6 d-flex justify-content-end">
          <SearchBar @search="$emit('search')" />
          <Button @search="$emit('search')" />
        </div>
      </div>
    </div>

  </header>

</template>

<style></style>