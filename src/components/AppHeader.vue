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

  <div class="bg-secondary">
    <SearchBar @search="$emit('search')" />
    <Button @search="$emit('search')" />
  </div>

</template>

<style></style>