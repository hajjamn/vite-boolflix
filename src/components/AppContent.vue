<script>
import ContentCard from './ContentCard.vue'
import { store } from '../store.js'

export default {
  components: {
    ContentCard
  },
  data() {
    return {
      store,
    }
  }
}

</script>

<template>

  <div class="bg-primary">
    <p>I am the content</p>
  </div>

  <h1>Films</h1>
  <ContentCard v-for="movie in store.movieSearchResults" :item="movie" :key="movie.id"></ContentCard>

</template>

<style></style>