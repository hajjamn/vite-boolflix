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

  <main>
    <div class="container" v-if="store.movieSearchResults.length > 0">
      <h2 class="text-center">Film</h2>
      <div class="row justify-content-center">
        <ContentCard v-for="movie in store.movieSearchResults" :item="movie" :searchType="'movie'" :key="movie.id">
        </ContentCard>
      </div>
    </div>

    <div class="container" v-if="store.tvSearchResults.length > 0">
      <h2 class="text-center">TV</h2>
      <div class="row justify-content-center">
        <ContentCard v-for="tv in store.tvSearchResults" :item="tv" :searchType="'tv'" :key="tv.id"></ContentCard>
      </div>

    </div>
  </main>

</template>

<style></style>