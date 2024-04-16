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

  <div class="row">
    <div class="w-50">
      <h2>Film</h2>
      <ContentCard v-for="movie in store.movieSearchResults" :item="movie" :searchType="'movie'" :key="movie.id">
      </ContentCard>
    </div>

    <div class="w-50">
      <h2>TV</h2>
      <ContentCard v-for="tv in store.tvSearchResults" :item="tv" :searchType="'tv'" :key="tv.id"></ContentCard>
    </div>
  </div>


</template>

<style></style>